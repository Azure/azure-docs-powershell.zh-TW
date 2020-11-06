---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2dd97b310de764638fab029c60407c578287e9a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447830"
---
# <span data-ttu-id="a0175-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="a0175-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="a0175-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0175-102">SYNOPSIS</span></span>
<span data-ttu-id="a0175-103">建立新的 Azure Data Lake Analytics 編目認證。</span><span class="sxs-lookup"><span data-stu-id="a0175-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0175-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0175-104">SYNTAX</span></span>

### <span data-ttu-id="a0175-105">CreateByHostNameAndPort (預設) </span><span class="sxs-lookup"><span data-stu-id="a0175-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0175-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="a0175-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0175-107">說明</span><span class="sxs-lookup"><span data-stu-id="a0175-107">DESCRIPTION</span></span>
<span data-ttu-id="a0175-108">New-AzureRmDataLakeAnalyticsCatalogCredential Cmdlet 會建立新的認證，以便在 Azure Data Lake Analytics 目錄中用來連線到外部資料源。</span><span class="sxs-lookup"><span data-stu-id="a0175-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="a0175-109">示例</span><span class="sxs-lookup"><span data-stu-id="a0175-109">EXAMPLES</span></span>

### <span data-ttu-id="a0175-110">範例1：為指定主機和埠的目錄建立認證</span><span class="sxs-lookup"><span data-stu-id="a0175-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="a0175-111">這個命令會使用 HTTPs 通訊協定，為指定的帳號、資料庫、主機和埠建立指定的認證。</span><span class="sxs-lookup"><span data-stu-id="a0175-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="a0175-112">範例2：針對指定完整 URI 的目錄建立認證</span><span class="sxs-lookup"><span data-stu-id="a0175-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="a0175-113">這個命令會針對指定的帳號、資料庫及外部資料源 URI 建立指定的認證。</span><span class="sxs-lookup"><span data-stu-id="a0175-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="a0175-114">參數</span><span class="sxs-lookup"><span data-stu-id="a0175-114">PARAMETERS</span></span>

### <span data-ttu-id="a0175-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a0175-115">-Account</span></span>
<span data-ttu-id="a0175-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a0175-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-117">-認證</span><span class="sxs-lookup"><span data-stu-id="a0175-117">-Credential</span></span>
<span data-ttu-id="a0175-118">指定認證的使用者名稱和對應密碼。</span><span class="sxs-lookup"><span data-stu-id="a0175-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a0175-119">-CredentialName</span></span>
<span data-ttu-id="a0175-120">指定認證的名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="a0175-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="a0175-121">-DatabaseHost</span></span>
<span data-ttu-id="a0175-122">指定認證可以連線至 mydatabase.contoso.com [格式] 的外部資料源的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a0175-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0175-123">-DatabaseName</span></span>
<span data-ttu-id="a0175-124">指定要儲存認證之 Data Lake Analytics acocunt 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a0175-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0175-125">-DefaultProfile</span></span>
<span data-ttu-id="a0175-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a0175-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-127">-埠</span><span class="sxs-lookup"><span data-stu-id="a0175-127">-Port</span></span>
<span data-ttu-id="a0175-128">指定使用此認證連接至指定 DatabaseHost 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a0175-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="a0175-129">-Uri</span></span>
<span data-ttu-id="a0175-130">指定此認證可連線的外部資料源 (URI) 的完整統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="a0175-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a0175-131">-Confirm</span></span>
<span data-ttu-id="a0175-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0175-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0175-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0175-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0175-134">CommonParameters</span></span>
<span data-ttu-id="a0175-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0175-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0175-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0175-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0175-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a0175-137">INPUTS</span></span>

### <span data-ttu-id="a0175-138">所有</span><span class="sxs-lookup"><span data-stu-id="a0175-138">None</span></span>
<span data-ttu-id="a0175-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a0175-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0175-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a0175-140">OUTPUTS</span></span>

### <span data-ttu-id="a0175-141">所有</span><span class="sxs-lookup"><span data-stu-id="a0175-141">None</span></span>

## <span data-ttu-id="a0175-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a0175-142">NOTES</span></span>

## <span data-ttu-id="a0175-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0175-143">RELATED LINKS</span></span>

