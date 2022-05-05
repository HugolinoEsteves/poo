import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class Connectionpsql {
	private Connection con = null;

	  private String hostName = null;
	  private String userName = null;
	  private String password = null;
	  private String url = null;
	  private String jdbcDriver = null;
	  private String dataBaseName = null;
	  private String dataBasePrefix = null;
	  private String dabaBasePort = null;
	  
	  public Connectionpsql() {
		  super();

		  hostName = "localhost";
		  userName = "POO";
		  password = "POO";
		  jdbcDriver = "org.postgresql.Driver";
		  dataBaseName = "POO";
		  dataBasePrefix = "jdbc:postgresql://";
		  dabaBasePort = "5432";

		  url = dataBasePrefix + hostName + ":"+dabaBasePort+"/" + dataBaseName + "/";   

		}

		public Connection getConnectionpsql() {
		  try {
		    if (con == null) {
		    	Class.forName(jdbcDriver);
		      con = DriverManager.getConnection(url, userName, password);
		    } else if (con.isClosed()) {
		      con = null;
		      return con ;
		    }
		  } catch (ClassNotFoundException e) {

		    

		    e.printStackTrace();
		  } catch (SQLException e) {

		   

			  e.printStackTrace();
		  }
		  return con;
		}
		public void closeConnection() {
			  if (con != null) {
			    try {
			      con.close();
			    } catch (SQLException e) {
			    
			      e.printStackTrace();
			    }
			  }
			}
	  
}


