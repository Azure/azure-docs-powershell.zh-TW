---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 838ebb56f52aa34bc1fe6016a8bf4f4966f4428d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447829"
---
# <span data-ttu-id="519dc-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="519dc-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="519dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="519dc-102">SYNOPSIS</span></span>
<span data-ttu-id="519dc-103">建立資料 Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="519dc-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="519dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="519dc-104">SYNTAX</span></span>

### <span data-ttu-id="519dc-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="519dc-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519dc-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="519dc-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="519dc-107">說明</span><span class="sxs-lookup"><span data-stu-id="519dc-107">DESCRIPTION</span></span>
<span data-ttu-id="519dc-108">**新的 AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet 會建立要在 Azure Data Lake Analytics 目錄中使用的秘密。</span><span class="sxs-lookup"><span data-stu-id="519dc-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="519dc-109">示例</span><span class="sxs-lookup"><span data-stu-id="519dc-109">EXAMPLES</span></span>

### <span data-ttu-id="519dc-110">範例1：取得目錄的機密</span><span class="sxs-lookup"><span data-stu-id="519dc-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="519dc-111">這個命令會取得與指定的帳號、資料庫、認證及主機相對應的密碼。</span><span class="sxs-lookup"><span data-stu-id="519dc-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="519dc-112">參數</span><span class="sxs-lookup"><span data-stu-id="519dc-112">PARAMETERS</span></span>

### <span data-ttu-id="519dc-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="519dc-113">-Account</span></span>
<span data-ttu-id="519dc-114">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="519dc-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="519dc-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="519dc-115">-DatabaseHost</span></span>
<span data-ttu-id="519dc-116">以 [mydatabase.contoso.com] 格式指定該機密所關聯之資料庫的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="519dc-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519dc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="519dc-117">-DatabaseName</span></span>
<span data-ttu-id="519dc-118">指定儲存秘密之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="519dc-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="519dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519dc-119">-DefaultProfile</span></span>
<span data-ttu-id="519dc-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="519dc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="519dc-121">-埠</span><span class="sxs-lookup"><span data-stu-id="519dc-121">-Port</span></span>
<span data-ttu-id="519dc-122">指定機密的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="519dc-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519dc-123">密碼</span><span class="sxs-lookup"><span data-stu-id="519dc-123">-Secret</span></span>
<span data-ttu-id="519dc-124">指定密碼的名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="519dc-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519dc-125">-Uri</span><span class="sxs-lookup"><span data-stu-id="519dc-125">-Uri</span></span>
<span data-ttu-id="519dc-126">指定機密的統一資源識別項 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="519dc-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519dc-127">CommonParameters</span></span>
<span data-ttu-id="519dc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="519dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519dc-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="519dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519dc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="519dc-130">INPUTS</span></span>

### <span data-ttu-id="519dc-131">所有</span><span class="sxs-lookup"><span data-stu-id="519dc-131">None</span></span>
<span data-ttu-id="519dc-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="519dc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="519dc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="519dc-133">OUTPUTS</span></span>

### <span data-ttu-id="519dc-134">所有</span><span class="sxs-lookup"><span data-stu-id="519dc-134">None</span></span>

## <span data-ttu-id="519dc-135">筆記</span><span class="sxs-lookup"><span data-stu-id="519dc-135">NOTES</span></span>

## <span data-ttu-id="519dc-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="519dc-136">RELATED LINKS</span></span>

[<span data-ttu-id="519dc-137">移除-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="519dc-137">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="519dc-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="519dc-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


