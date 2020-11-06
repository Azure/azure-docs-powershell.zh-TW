---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 22a10d4f65d43f4d11871cbf43399bfc35febf04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454616"
---
# <span data-ttu-id="d825c-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d825c-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="d825c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d825c-102">SYNOPSIS</span></span>
<span data-ttu-id="d825c-103">修改資料 Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="d825c-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d825c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d825c-104">SYNTAX</span></span>

### <span data-ttu-id="d825c-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="d825c-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d825c-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="d825c-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d825c-107">說明</span><span class="sxs-lookup"><span data-stu-id="d825c-107">DESCRIPTION</span></span>
<span data-ttu-id="d825c-108">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet 會修改與 Azure Data Lake Analytics 目錄相關聯的機密。</span><span class="sxs-lookup"><span data-stu-id="d825c-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="d825c-109">示例</span><span class="sxs-lookup"><span data-stu-id="d825c-109">EXAMPLES</span></span>

### <span data-ttu-id="d825c-110">範例1：修改與帳戶相關聯的秘密</span><span class="sxs-lookup"><span data-stu-id="d825c-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="d825c-111">這個命令會設定與資料 Lake Analytics 目錄相關聯的機密。</span><span class="sxs-lookup"><span data-stu-id="d825c-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="d825c-112">參數</span><span class="sxs-lookup"><span data-stu-id="d825c-112">PARAMETERS</span></span>

### <span data-ttu-id="d825c-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d825c-113">-Account</span></span>
<span data-ttu-id="d825c-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d825c-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d825c-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="d825c-115">-DatabaseHost</span></span>
<span data-ttu-id="d825c-116">以 [mydatabase.contoso.com] 格式指定該機密所關聯之資料庫的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d825c-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d825c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d825c-117">-DatabaseName</span></span>
<span data-ttu-id="d825c-118">指定存放秘密之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d825c-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="d825c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d825c-119">-DefaultProfile</span></span>
<span data-ttu-id="d825c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d825c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d825c-121">-埠</span><span class="sxs-lookup"><span data-stu-id="d825c-121">-Port</span></span>
<span data-ttu-id="d825c-122">指定機密的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d825c-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullUri
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d825c-123">密碼</span><span class="sxs-lookup"><span data-stu-id="d825c-123">-Secret</span></span>
<span data-ttu-id="d825c-124">指定密碼的名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="d825c-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="d825c-125">-Uri</span><span class="sxs-lookup"><span data-stu-id="d825c-125">-Uri</span></span>
<span data-ttu-id="d825c-126">指定機密的統一資源識別項 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="d825c-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d825c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d825c-127">CommonParameters</span></span>
<span data-ttu-id="d825c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d825c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d825c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d825c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d825c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d825c-130">INPUTS</span></span>

### <span data-ttu-id="d825c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="d825c-131">System.String</span></span>

### <span data-ttu-id="d825c-132">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d825c-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="d825c-133">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="d825c-133">System.Uri</span></span>

### <span data-ttu-id="d825c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d825c-134">System.Int32</span></span>

## <span data-ttu-id="d825c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d825c-135">OUTPUTS</span></span>

### <span data-ttu-id="d825c-136">[DataLake. USqlSecret]。</span><span class="sxs-lookup"><span data-stu-id="d825c-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="d825c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d825c-137">NOTES</span></span>

## <span data-ttu-id="d825c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d825c-138">RELATED LINKS</span></span>

[<span data-ttu-id="d825c-139">新-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d825c-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="d825c-140">移除-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="d825c-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


