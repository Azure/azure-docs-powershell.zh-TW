---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613582"
---
# <span data-ttu-id="ed930-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="ed930-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="ed930-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed930-102">SYNOPSIS</span></span>
<span data-ttu-id="ed930-103">將 JSON 格式的藍圖檔案匯入至藍圖物件，然後將它儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="ed930-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="ed930-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed930-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed930-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed930-105">DESCRIPTION</span></span>
<span data-ttu-id="ed930-106">匯入藍圖定義及其專案。</span><span class="sxs-lookup"><span data-stu-id="ed930-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="ed930-107">示例</span><span class="sxs-lookup"><span data-stu-id="ed930-107">EXAMPLES</span></span>

### <span data-ttu-id="ed930-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ed930-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="ed930-109">匯入藍圖定義及其工件，並儲存在訂閱中。</span><span class="sxs-lookup"><span data-stu-id="ed930-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="ed930-110">參數</span><span class="sxs-lookup"><span data-stu-id="ed930-110">PARAMETERS</span></span>

### <span data-ttu-id="ed930-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed930-111">-DefaultProfile</span></span>
<span data-ttu-id="ed930-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed930-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ed930-113">-Force</span></span>
<span data-ttu-id="ed930-114">當設定為 true 時，執行將不要求確認。</span><span class="sxs-lookup"><span data-stu-id="ed930-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="ed930-115">-InputPath</span></span>
<span data-ttu-id="ed930-116">磁片上藍圖 JSON 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed930-116">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ed930-117">-ManagementGroupId</span></span>
<span data-ttu-id="ed930-118">已儲存藍圖定義或將要儲存的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed930-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed930-119">-Name</span></span>
<span data-ttu-id="ed930-120">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ed930-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed930-121">-SubscriptionId</span></span>
<span data-ttu-id="ed930-122">藍圖定義或將要儲存的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="ed930-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed930-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed930-123">CommonParameters</span></span>
<span data-ttu-id="ed930-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed930-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed930-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed930-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed930-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ed930-126">INPUTS</span></span>

### <span data-ttu-id="ed930-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ed930-127">System.String</span></span>

## <span data-ttu-id="ed930-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ed930-128">OUTPUTS</span></span>

### <span data-ttu-id="ed930-129">System.object</span><span class="sxs-lookup"><span data-stu-id="ed930-129">System.String</span></span>

## <span data-ttu-id="ed930-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ed930-130">NOTES</span></span>

## <span data-ttu-id="ed930-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed930-131">RELATED LINKS</span></span>
