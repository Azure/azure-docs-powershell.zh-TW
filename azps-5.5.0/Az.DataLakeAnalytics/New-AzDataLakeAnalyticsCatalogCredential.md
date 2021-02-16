---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141046"
---
# <span data-ttu-id="1fd8d-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="1fd8d-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="1fd8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd8d-103">建立新的 Azure Data Lake Analytics 編目認證。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="1fd8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fd8d-104">SYNTAX</span></span>

### <span data-ttu-id="1fd8d-105">CreateByHostNameAndPort (預設) </span><span class="sxs-lookup"><span data-stu-id="1fd8d-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd8d-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="1fd8d-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd8d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1fd8d-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd8d-108">New-AzDataLakeAnalyticsCatalogCredential Cmdlet 會建立新的認證，以便在 Azure Data Lake Analytics 目錄中用來連線到外部資料源。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="1fd8d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1fd8d-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd8d-110">範例1：為指定主機和埠的目錄建立認證</span><span class="sxs-lookup"><span data-stu-id="1fd8d-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="1fd8d-111">這個命令會使用 HTTPs 通訊協定，為指定的帳號、資料庫、主機和埠建立指定的認證。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="1fd8d-112">範例2：針對指定完整 URI 的目錄建立認證</span><span class="sxs-lookup"><span data-stu-id="1fd8d-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="1fd8d-113">這個命令會針對指定的帳號、資料庫及外部資料源 URI 建立指定的認證。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="1fd8d-114">參數</span><span class="sxs-lookup"><span data-stu-id="1fd8d-114">PARAMETERS</span></span>

### <span data-ttu-id="1fd8d-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="1fd8d-115">-Account</span></span>
<span data-ttu-id="1fd8d-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-117">-認證</span><span class="sxs-lookup"><span data-stu-id="1fd8d-117">-Credential</span></span>
<span data-ttu-id="1fd8d-118">指定認證的使用者名稱和對應密碼。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="1fd8d-119">-CredentialName</span></span>
<span data-ttu-id="1fd8d-120">指定認證的名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="1fd8d-121">-DatabaseHost</span></span>
<span data-ttu-id="1fd8d-122">指定認證可以連線至 mydatabase.contoso.com [格式] 的外部資料源的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fd8d-123">-DatabaseName</span></span>
<span data-ttu-id="1fd8d-124">指定要儲存認證之 Data Lake Analytics 帳戶中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd8d-125">-DefaultProfile</span></span>
<span data-ttu-id="1fd8d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1fd8d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fd8d-127">-埠</span><span class="sxs-lookup"><span data-stu-id="1fd8d-127">-Port</span></span>
<span data-ttu-id="1fd8d-128">指定使用此認證連接至指定 DatabaseHost 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="1fd8d-129">-Uri</span></span>
<span data-ttu-id="1fd8d-130">指定此認證可連線的外部資料源 (URI) 的完整統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="1fd8d-131">-Confirm</span></span>
<span data-ttu-id="1fd8d-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd8d-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd8d-134">CommonParameters</span></span>
<span data-ttu-id="1fd8d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd8d-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd8d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1fd8d-137">INPUTS</span></span>

### <span data-ttu-id="1fd8d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1fd8d-138">System.String</span></span>

### <span data-ttu-id="1fd8d-139">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1fd8d-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1fd8d-140">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="1fd8d-140">System.Uri</span></span>

### <span data-ttu-id="1fd8d-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1fd8d-141">System.Int32</span></span>

## <span data-ttu-id="1fd8d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1fd8d-142">OUTPUTS</span></span>

### <span data-ttu-id="1fd8d-143">[DataLake. USqlCredential]。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="1fd8d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1fd8d-144">NOTES</span></span>

## <span data-ttu-id="1fd8d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fd8d-145">RELATED LINKS</span></span>
