---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446698"
---
# <span data-ttu-id="21c3d-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="21c3d-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="21c3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="21c3d-103">更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="21c3d-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="21c3d-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="21c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="21c3d-106">**AzureRmOperationalInsightsSavedSearch** Cmdlet 會更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="21c3d-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="21c3d-107">示例</span><span class="sxs-lookup"><span data-stu-id="21c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="21c3d-108">範例1：使用更新的屬性設定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="21c3d-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="21c3d-109">這個命令會將已儲存的搜尋設定為已更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="21c3d-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="21c3d-110">參數</span><span class="sxs-lookup"><span data-stu-id="21c3d-110">PARAMETERS</span></span>

### <span data-ttu-id="21c3d-111">-類別</span><span class="sxs-lookup"><span data-stu-id="21c3d-111">-Category</span></span>
<span data-ttu-id="21c3d-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21c3d-113">-DisplayName</span></span>
<span data-ttu-id="21c3d-114">指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-114">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="21c3d-115">-ETag</span></span>
<span data-ttu-id="21c3d-116">指定 ETag 名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-116">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-117">-Query</span><span class="sxs-lookup"><span data-stu-id="21c3d-117">-Query</span></span>
<span data-ttu-id="21c3d-118">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-118">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="21c3d-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-120">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="21c3d-121">-SavedSearchId</span></span>
<span data-ttu-id="21c3d-122">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="21c3d-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="21c3d-123">-標記</span><span class="sxs-lookup"><span data-stu-id="21c3d-123">-Tags</span></span>
```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-124">-版本</span><span class="sxs-lookup"><span data-stu-id="21c3d-124">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21c3d-125">-WorkspaceName</span></span>
<span data-ttu-id="21c3d-126">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-126">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c3d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c3d-127">-DefaultProfile</span></span>
<span data-ttu-id="21c3d-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21c3d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c3d-129">CommonParameters</span></span>
<span data-ttu-id="21c3d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21c3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c3d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21c3d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c3d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="21c3d-132">INPUTS</span></span>

## <span data-ttu-id="21c3d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="21c3d-133">OUTPUTS</span></span>

## <span data-ttu-id="21c3d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="21c3d-134">NOTES</span></span>

## <span data-ttu-id="21c3d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="21c3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="21c3d-136">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21c3d-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


