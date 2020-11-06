---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e36030cbe1ccfe78db625d9d4142de13ba2f54ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446837"
---
# <span data-ttu-id="6221c-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="6221c-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="6221c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6221c-102">SYNOPSIS</span></span>
<span data-ttu-id="6221c-103">建立資料 Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="6221c-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6221c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6221c-104">SYNTAX</span></span>

### <span data-ttu-id="6221c-105">指定完整 URI</span><span class="sxs-lookup"><span data-stu-id="6221c-105">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6221c-106">指定主機名稱與埠</span><span class="sxs-lookup"><span data-stu-id="6221c-106">Specify host name and port</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6221c-107">說明</span><span class="sxs-lookup"><span data-stu-id="6221c-107">DESCRIPTION</span></span>
<span data-ttu-id="6221c-108">**新的 AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet 會建立要在 Azure Data Lake Analytics 目錄中使用的秘密。</span><span class="sxs-lookup"><span data-stu-id="6221c-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="6221c-109">示例</span><span class="sxs-lookup"><span data-stu-id="6221c-109">EXAMPLES</span></span>

### <span data-ttu-id="6221c-110">範例1：取得目錄的機密</span><span class="sxs-lookup"><span data-stu-id="6221c-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="6221c-111">這個命令會取得與指定的帳號、資料庫、認證及主機相對應的密碼。</span><span class="sxs-lookup"><span data-stu-id="6221c-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="6221c-112">參數</span><span class="sxs-lookup"><span data-stu-id="6221c-112">PARAMETERS</span></span>

### <span data-ttu-id="6221c-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6221c-113">-Account</span></span>
<span data-ttu-id="6221c-114">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6221c-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6221c-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="6221c-115">-DatabaseHost</span></span>
<span data-ttu-id="6221c-116">以 [mydatabase.contoso.com] 格式指定該機密所關聯之資料庫的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6221c-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6221c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6221c-117">-DatabaseName</span></span>
<span data-ttu-id="6221c-118">指定儲存秘密之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6221c-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="6221c-119">-埠</span><span class="sxs-lookup"><span data-stu-id="6221c-119">-Port</span></span>
<span data-ttu-id="6221c-120">指定機密的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="6221c-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6221c-121">密碼</span><span class="sxs-lookup"><span data-stu-id="6221c-121">-Secret</span></span>
<span data-ttu-id="6221c-122">指定密碼的名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="6221c-122">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6221c-123">-Uri</span><span class="sxs-lookup"><span data-stu-id="6221c-123">-Uri</span></span>
<span data-ttu-id="6221c-124">指定機密的統一資源識別項 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="6221c-124">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6221c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6221c-125">-DefaultProfile</span></span>
<span data-ttu-id="6221c-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6221c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6221c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6221c-127">CommonParameters</span></span>
<span data-ttu-id="6221c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6221c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6221c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6221c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6221c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6221c-130">INPUTS</span></span>

## <span data-ttu-id="6221c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6221c-131">OUTPUTS</span></span>

### <span data-ttu-id="6221c-132">所有</span><span class="sxs-lookup"><span data-stu-id="6221c-132">None</span></span>

## <span data-ttu-id="6221c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6221c-133">NOTES</span></span>

## <span data-ttu-id="6221c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6221c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6221c-135">移除-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="6221c-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="6221c-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="6221c-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)

