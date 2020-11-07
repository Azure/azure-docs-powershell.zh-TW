---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 54a759370f39dcd3844d42d858d23f6c178a4d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624152"
---
# New-AzureRmDataFactoryEncryptValue

## 摘要
加密機密資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByFactoryName (預設) 
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDataFactoryEncryptValue** Cmdlet 會加密機密資料（例如密碼或 Microsoft SQL Server 連接字串），並傳回加密的值。

## 示例

### 範例1：加密非 ODBC 連接字串
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

第一個命令使用 ConvertTo-SecureString Cmdlet，將指定的連接字串轉換為 **SecureString** 物件，然後將該物件儲存在 $Value 變數中。
如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。
允許的值： [SQL Server] 或 [Oracle 連接字串]。

第二個命令會針對指定資料工廠、閘道、資源群組及連結的服務類型，為儲存在 $Value 中的物件建立加密的值。

### 範例2：加密使用 Windows 驗證的非 ODBC 連接字串。
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

第一個命令使用 **ConvertTo-SecureString** ，將指定的連接字串轉換為安全的字串物件，然後將該物件儲存在 $Value 變數中。

第二個命令使用 Get-Credential Cmdlet 來收集 windows 驗證 (的使用者名稱和密碼) ，然後將該 **PSCredential** 物件儲存在 $Credential 變數中。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

第三個命令會針對儲存在 $Value 中的物件，$Credential 以及針對指定資料工廠、閘道、資源群組及連結的服務類型，建立加密的值。

### 範例3：加密檔案系統連結服務的伺服器名稱和認證
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

第一個命令使用 **ConvertTo-SecureString** ，將指定的字串轉換成安全的字串，然後將該物件儲存在 $Value 變數中。

第二個命令使用 **取得認證** 來收集 windows 驗證 (的使用者名稱和密碼) ，然後將該 **PSCredential** 物件儲存在 $Credential 變數中。

第三個命令會針對儲存在 $Value 中的物件，$Credential 以及針對指定資料工廠、閘道、資源群組及連結的服務類型，建立加密的值。

### 範例4：加密 HDFS 連結服務的認證
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

**ConvertTo-SecureString** 命令會將指定的字串轉換為安全字串。
[ **新物件** ] 命令會使用安全的使用者名稱和密碼字串建立一個 PSCredential 物件。
相反地，您可以使用 [ **取得認證** ] 命令，在 (的使用者名稱和密碼) 中收集 windows 驗證，然後將傳回的 **PSCredential** 物件儲存在 $credential 變數中，如先前的範例所示。

**新的-AzureRmDataFactoryEncryptValue** 命令會針對指定資料工廠、閘道、資源群組及連結的服務類型，為儲存在 $Credential 中的物件建立加密的值。

### 範例5：加密 ODBC 連結服務的認證
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

**ConvertTo-SecureString** 命令會將指定的字串轉換為安全字串。

**新的-AzureRmDataFactoryEncryptValue** 命令會針對指定資料工廠、閘道、資源群組及連結的服務類型，為儲存在 $Value 中的物件建立加密的值。

## 參數

### -AuthenticationType
指定要用來連接至資料來源的驗證類型。
此參數可接受的值為：

- 時間
- 空白
- 匿名.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -認證
指定要使用的 [Windows 驗證認證] ([使用者名稱] 和 [密碼]) 。
這個 Cmdlet 會加密您在此處指定的認證資料。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -資料庫
指定連結服務的資料庫名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
指定 **PSDataFactory** 物件。
這個 Cmdlet 會針對此參數指定的資料工廠加密資料。

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
指定資料工廠的名稱。
這個 Cmdlet 會針對此參數指定的資料工廠加密資料。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewayName
指定閘道的名稱。
這個 Cmdlet 會加密此參數指定之閘道的資料。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
指定開放式資料庫連線 (ODBC) 連接字串的非認證部分。
這個參數只適用于 ODBC 連結的服務。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱。
這個 Cmdlet 會加密此參數指定之群組的資料。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -伺服器
指定連結服務的伺服器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -類型
指定連結的服務類型。
這個 Cmdlet 會針對此參數指定的連結服務類型來加密資料。
此參數可接受的值為：

- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -值
指定要加密的值。
針對內部部署的 SQL Server 連結服務和內部部署的 Oracle 連結服務，請使用連接字串。
針對內部部署的 ODBC 連結服務，請使用連線字串的 credential 部分。
針對內部部署檔案系統連結的服務，如果檔案系統是閘道電腦的本機，請使用本機或 localhost，如果檔案系統位於與閘道電腦不同的伺服器上，請使用 \\ \\ 伺服器名稱。

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### System.object

## 筆記
* 關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結

[新-AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


