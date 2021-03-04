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
# <span data-ttu-id="1136b-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="1136b-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="1136b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1136b-102">SYNOPSIS</span></span>
<span data-ttu-id="1136b-103">加密機密資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="1136b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1136b-104">SYNTAX</span></span>

### <span data-ttu-id="1136b-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1136b-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1136b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1136b-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1136b-107">描述</span><span class="sxs-lookup"><span data-stu-id="1136b-107">DESCRIPTION</span></span>
<span data-ttu-id="1136b-108">**New-AzDataFactoryEncryptValue** Cmdlet 會加密機密資料，例如密碼或 Microsoft SQL Server 連接字串，並返回加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="1136b-109">例子</span><span class="sxs-lookup"><span data-stu-id="1136b-109">EXAMPLES</span></span>

### <span data-ttu-id="1136b-110">範例 1：加密非 ODBC 連接字串</span><span class="sxs-lookup"><span data-stu-id="1136b-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="1136b-111">第一個命令使用 ConvertTo-SecureString Cmdlet 將指定的連接字串轉換為 **SecureString** 物件，然後將該物件儲存在 $Value 變數中。</span><span class="sxs-lookup"><span data-stu-id="1136b-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="1136b-112">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1136b-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1136b-113">允許的值：SQL Server 或 Oracle 連接字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="1136b-114">第二個命令會為儲存在 $Value 中指定資料工廠、閘道、資源群組和連結服務類型的物件建立加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="1136b-115">範例 2：加密使用 Windows 驗證的非 ODBC 連接字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="1136b-116">第一個命令使用 **ConvertTo-SecureString** 將指定的連接字串轉換為安全字串物件，然後將該物件儲存在 $Value 變數中。</span><span class="sxs-lookup"><span data-stu-id="1136b-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="1136b-117">第二個命令使用 Get-Credential Cmdlet 收集 windows 驗證 (使用者名稱和密碼) ，然後將 **該 PSCredential** 物件儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1136b-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="1136b-118">如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="1136b-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="1136b-119">第三個命令會為儲存在 $Value 和 $Credential 中指定資料工廠、閘道、資源群組及連結服務類型的物件建立加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="1136b-120">範例 3：加密檔案系統連結服務的伺服器名稱和認證</span><span class="sxs-lookup"><span data-stu-id="1136b-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="1136b-121">第一個命令使用 **ConvertTo-SecureString** 將指定的字串轉換為安全字串，然後將該物件儲存在$Value變數。</span><span class="sxs-lookup"><span data-stu-id="1136b-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="1136b-122">第二個命令使用 **Get-Credential** 收集 Windows 驗證 (使用者名稱和密碼) ，然後將 **該 PSCredential** 物件儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1136b-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="1136b-123">第三個命令會為儲存在 $Value 和 $Credential 中指定資料工廠、閘道、資源群組及連結服務類型的物件建立加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="1136b-124">範例 4：加密 HDFS 連結服務的認證</span><span class="sxs-lookup"><span data-stu-id="1136b-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="1136b-125">**ConvertTo-SecureString 命令** 會將指定的字串轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="1136b-126">**New-Object 命令** 會使用安全的使用者名稱和密碼字串建立 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="1136b-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="1136b-127">您可以改為使用 **Get-Credential** 命令收集 Windows 驗證 (使用者名稱和密碼) ，然後將所返回 **的 PSCredential** 物件儲存在 $credential 變數中，如先前的範例所示。</span><span class="sxs-lookup"><span data-stu-id="1136b-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="1136b-128">**New-AzDataFactoryEncryptValue** 命令會針對指定的資料工廠、閘道、資源群組及連結服務類型，為儲存在 $Credential 中的物件建立加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="1136b-129">範例 5：加密 ODBC 連結服務的認證</span><span class="sxs-lookup"><span data-stu-id="1136b-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="1136b-130">**ConvertTo-SecureString 命令** 會將指定的字串轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="1136b-131">**New-AzDataFactoryEncryptValue** 命令會針對指定的資料工廠、閘道、資源群組及連結服務類型，為儲存在 $Value 中的物件建立加密值。</span><span class="sxs-lookup"><span data-stu-id="1136b-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="1136b-132">參數</span><span class="sxs-lookup"><span data-stu-id="1136b-132">PARAMETERS</span></span>

### <span data-ttu-id="1136b-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1136b-133">-AuthenticationType</span></span>
<span data-ttu-id="1136b-134">指定要用來連接到資料來源的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="1136b-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="1136b-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1136b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1136b-136">窗戶</span><span class="sxs-lookup"><span data-stu-id="1136b-136">Windows</span></span>
- <span data-ttu-id="1136b-137">基本</span><span class="sxs-lookup"><span data-stu-id="1136b-137">Basic</span></span>
- <span data-ttu-id="1136b-138">匿名。</span><span class="sxs-lookup"><span data-stu-id="1136b-138">Anonymous.</span></span>

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

### <span data-ttu-id="1136b-139">-認證</span><span class="sxs-lookup"><span data-stu-id="1136b-139">-Credential</span></span>
<span data-ttu-id="1136b-140">指定 Windows 驗證認證 (使用者名稱和密碼) 使用。</span><span class="sxs-lookup"><span data-stu-id="1136b-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="1136b-141">此 Cmdlet 會加密您在此處指定的認證資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-141">This cmdlet encrypts the credential data you specify here.</span></span>

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

### <span data-ttu-id="1136b-142">-資料庫</span><span class="sxs-lookup"><span data-stu-id="1136b-142">-Database</span></span>
<span data-ttu-id="1136b-143">指定連結服務的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-143">Specifies the database name of the linked service.</span></span>

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

### <span data-ttu-id="1136b-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1136b-144">-DataFactory</span></span>
<span data-ttu-id="1136b-145">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="1136b-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1136b-146">此 Cmdlet 會加密此參數指定之資料工廠的資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1136b-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1136b-147">-DataFactoryName</span></span>
<span data-ttu-id="1136b-148">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1136b-149">此 Cmdlet 會加密此參數指定之資料工廠的資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1136b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1136b-150">-DefaultProfile</span></span>
<span data-ttu-id="1136b-151">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1136b-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1136b-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="1136b-152">-GatewayName</span></span>
<span data-ttu-id="1136b-153">指定閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="1136b-154">此 Cmdlet 會加密此參數指定之閘道的資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="1136b-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="1136b-155">-NonCredentialValue</span></span>
<span data-ttu-id="1136b-156">指定 Open Database Connectivity 的非認證部分 (ODBC) 字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="1136b-157">此參數僅適用于 ODBC 連結服務。</span><span class="sxs-lookup"><span data-stu-id="1136b-157">This parameter is applicable only for the ODBC linked service.</span></span>

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

### <span data-ttu-id="1136b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1136b-158">-ResourceGroupName</span></span>
<span data-ttu-id="1136b-159">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1136b-160">此 Cmdlet 會加密此參數指定之群組的資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1136b-161">-Server</span><span class="sxs-lookup"><span data-stu-id="1136b-161">-Server</span></span>
<span data-ttu-id="1136b-162">指定連結服務的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-162">Specifies the server name of the linked service.</span></span>

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

### <span data-ttu-id="1136b-163">-類型</span><span class="sxs-lookup"><span data-stu-id="1136b-163">-Type</span></span>
<span data-ttu-id="1136b-164">指定連結的服務類型。</span><span class="sxs-lookup"><span data-stu-id="1136b-164">Specifies the linked service type.</span></span>
<span data-ttu-id="1136b-165">此 Cmdlet 會針對此參數指定的連結服務類型加密資料。</span><span class="sxs-lookup"><span data-stu-id="1136b-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="1136b-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1136b-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1136b-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="1136b-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="1136b-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="1136b-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="1136b-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="1136b-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="1136b-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="1136b-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="1136b-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="1136b-175">OnPremisesSybaseLinkedService</span></span>

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

### <span data-ttu-id="1136b-176">-值</span><span class="sxs-lookup"><span data-stu-id="1136b-176">-Value</span></span>
<span data-ttu-id="1136b-177">指定要加密的值。</span><span class="sxs-lookup"><span data-stu-id="1136b-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="1136b-178">針對內部部署 SQL Server 連結服務和內部部署 Oracle 連結服務，請使用連接字串。</span><span class="sxs-lookup"><span data-stu-id="1136b-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="1136b-179">針對內部部署 ODBC 連結服務，請使用連接字串的認證部分。</span><span class="sxs-lookup"><span data-stu-id="1136b-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="1136b-180">如果是內部部署檔案系統連結服務，如果檔案系統是閘道電腦的本地，請使用 Local 或 localhost，如果檔案系統位於與閘道電腦不同的伺服器上，請使用 \\ \\ 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1136b-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

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

### <span data-ttu-id="1136b-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1136b-181">CommonParameters</span></span>
<span data-ttu-id="1136b-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1136b-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1136b-183">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1136b-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1136b-184">輸入</span><span class="sxs-lookup"><span data-stu-id="1136b-184">INPUTS</span></span>

### <span data-ttu-id="1136b-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1136b-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1136b-186">System.String</span><span class="sxs-lookup"><span data-stu-id="1136b-186">System.String</span></span>

## <span data-ttu-id="1136b-187">輸出</span><span class="sxs-lookup"><span data-stu-id="1136b-187">OUTPUTS</span></span>

### <span data-ttu-id="1136b-188">System.String</span><span class="sxs-lookup"><span data-stu-id="1136b-188">System.String</span></span>

## <span data-ttu-id="1136b-189">筆記</span><span class="sxs-lookup"><span data-stu-id="1136b-189">NOTES</span></span>
* <span data-ttu-id="1136b-190">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="1136b-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1136b-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="1136b-191">RELATED LINKS</span></span>

[<span data-ttu-id="1136b-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="1136b-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


