---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 9a1f2bac984b4cad5267775dcbe59e79ed0eb677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907666"
---
# New-AzDataFactoryEncryptValue

## 簡介
加密機密資料。

## 語法

### ByFactoryName (預設) 
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzDataFactoryEncryptValue** Cmdlet 會加密機密資料，例如密碼或 Microsoft SQL Server 連接字串，並返回加密值。

## 例子

### 範例 1：加密非 ODBC 連接字串
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

第一個命令使用 ConvertTo-SecureString Cmdlet 將指定的連接字串轉換為 **SecureString** 物件，然後將該物件儲存在 $Value 變數中。
如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。
允許的值：SQL Server 或 Oracle 連接字串。
第二個命令會為儲存在 $Value 中指定資料工廠、閘道、資源群組和連結服務類型的物件建立加密值。

### 範例 2：加密使用 Windows 驗證的非 ODBC 連接字串。
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

第一個命令使用 **ConvertTo-SecureString** 將指定的連接字串轉換為安全字串物件，然後將該物件儲存在 $Value 變數中。
第二個命令使用 Get-Credential Cmdlet 收集 windows 驗證 (使用者名稱和密碼) ，然後將 **該 PSCredential** 物件儲存在 $Credential 變數中。
如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。
第三個命令會為儲存在 $Value 和 $Credential 中指定資料工廠、閘道、資源群組及連結服務類型的物件建立加密值。

### 範例 3：加密檔案系統連結服務的伺服器名稱和認證
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

第一個命令使用 **ConvertTo-SecureString** 將指定的字串轉換為安全字串，然後將該物件儲存在$Value變數。
第二個命令使用 **Get-Credential** 收集 Windows 驗證 (使用者名稱和密碼) ，然後將 **該 PSCredential** 物件儲存在 $Credential 變數中。
第三個命令會為儲存在 $Value 和 $Credential 中指定資料工廠、閘道、資源群組及連結服務類型的物件建立加密值。

### 範例 4：加密 HDFS 連結服務的認證
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

**ConvertTo-SecureString 命令** 會將指定的字串轉換為安全字串。
**New-Object 命令** 會使用安全的使用者名稱和密碼字串建立 PSCredential 物件。
您可以改為使用 **Get-Credential** 命令收集 Windows 驗證 (使用者名稱和密碼) ，然後將所返回 **的 PSCredential** 物件儲存在 $credential 變數中，如先前的範例所示。
**New-AzDataFactoryEncryptValue** 命令會針對指定的資料工廠、閘道、資源群組及連結服務類型，為儲存在 $Credential 中的物件建立加密值。

### 範例 5：加密 ODBC 連結服務的認證
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

**ConvertTo-SecureString 命令** 會將指定的字串轉換為安全字串。
**New-AzDataFactoryEncryptValue** 命令會針對指定的資料工廠、閘道、資源群組及連結服務類型，為儲存在 $Value 中的物件建立加密值。

## 參數

### -AuthenticationType
指定要用來連接到資料來源的驗證類型。
此參數可接受的值為：
- 窗戶
- 基本
- 匿名。

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
指定 Windows 驗證認證 (使用者名稱和密碼) 使用。
此 Cmdlet 會加密您在此處指定的認證資料。

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
此 Cmdlet 會加密此參數指定之資料工廠的資料。

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
此 Cmdlet 會加密此參數指定之資料工廠的資料。

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

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
指定閘道的名稱。
此 Cmdlet 會加密此參數指定之閘道的資料。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
指定 Open Database Connectivity 的非認證部分 (ODBC) 字串。
此參數僅適用于 ODBC 連結服務。

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
指定 Azure 資源組的名稱。
此 Cmdlet 會加密此參數指定之群組的資料。

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

### -Server
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
此 Cmdlet 會針對此參數指定的連結服務類型加密資料。
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
針對內部部署 SQL Server 連結服務和內部部署 Oracle 連結服務，請使用連接字串。
針對內部部署 ODBC 連結服務，請使用連接字串的認證部分。
如果是內部部署檔案系統連結服務，如果檔案系統是閘道電腦的本地，請使用 Local 或 localhost，如果檔案系統位於與閘道電腦不同的伺服器上，請使用 \\ \\ 伺服器名稱。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 輸出

### System.String

## 筆記
* 關鍵字：azure、azurerm、arm、resource、management、manager、data、azure

## 相關連結

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


