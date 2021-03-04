---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908641"
---
# <span data-ttu-id="b3e29-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b3e29-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b3e29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3e29-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e29-103">將 JSON 格式的藍圖檔案匯出至藍圖物件，並將其儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="b3e29-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b3e29-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3e29-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e29-105">描述</span><span class="sxs-lookup"><span data-stu-id="b3e29-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e29-106">使用其產品來匯出藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="b3e29-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="b3e29-107">例子</span><span class="sxs-lookup"><span data-stu-id="b3e29-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e29-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3e29-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="b3e29-109">將藍圖定義及其產品一併儲存于訂閱中。</span><span class="sxs-lookup"><span data-stu-id="b3e29-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="b3e29-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3e29-110">PARAMETERS</span></span>

### <span data-ttu-id="b3e29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e29-111">-DefaultProfile</span></span>
<span data-ttu-id="b3e29-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3e29-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e29-113">-強制</span><span class="sxs-lookup"><span data-stu-id="b3e29-113">-Force</span></span>
<span data-ttu-id="b3e29-114">當設定為 True 時，執行不會要求確認。</span><span class="sxs-lookup"><span data-stu-id="b3e29-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="b3e29-115">-IncludeSubFolders</span></span>
<span data-ttu-id="b3e29-116">當設定為 True 時，子資料夾中的專案會包含在內。</span><span class="sxs-lookup"><span data-stu-id="b3e29-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b3e29-117">-InputPath</span></span>
<span data-ttu-id="b3e29-118">藍圖 JSON 檔案在磁片上的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3e29-118">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b3e29-119">-ManagementGroupId</span></span>
<span data-ttu-id="b3e29-120">儲存藍圖定義的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3e29-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3e29-121">-Name</span></span>
<span data-ttu-id="b3e29-122">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b3e29-122">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3e29-123">-PassThru</span></span>
<span data-ttu-id="b3e29-124">設定完成之後，Cmdlet 會返回代表已輸入藍圖定義的物件。</span><span class="sxs-lookup"><span data-stu-id="b3e29-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="b3e29-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b3e29-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3e29-126">-SubscriptionId</span></span>
<span data-ttu-id="b3e29-127">已儲存或將會儲存藍圖定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3e29-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e29-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b3e29-128">-Confirm</span></span>
<span data-ttu-id="b3e29-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3e29-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e29-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e29-130">-WhatIf</span></span>
<span data-ttu-id="b3e29-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3e29-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3e29-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3e29-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e29-133">CommonParameters</span></span>
<span data-ttu-id="b3e29-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3e29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e29-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e29-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e29-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b3e29-136">INPUTS</span></span>

### <span data-ttu-id="b3e29-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e29-137">System.String</span></span>

## <span data-ttu-id="b3e29-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b3e29-138">OUTPUTS</span></span>

### <span data-ttu-id="b3e29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e29-139">System.String</span></span>

## <span data-ttu-id="b3e29-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b3e29-140">NOTES</span></span>

## <span data-ttu-id="b3e29-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3e29-141">RELATED LINKS</span></span>
