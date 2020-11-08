---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137556"
---
# <span data-ttu-id="41d7b-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="41d7b-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="41d7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="41d7b-103">將 JSON 格式的藍圖檔案匯入至藍圖物件，然後將它儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="41d7b-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="41d7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="41d7b-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d7b-105">說明</span><span class="sxs-lookup"><span data-stu-id="41d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="41d7b-106">匯入藍圖定義及其專案。</span><span class="sxs-lookup"><span data-stu-id="41d7b-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="41d7b-107">示例</span><span class="sxs-lookup"><span data-stu-id="41d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="41d7b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="41d7b-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="41d7b-109">匯入藍圖定義及其工件，並儲存在訂閱中。</span><span class="sxs-lookup"><span data-stu-id="41d7b-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="41d7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="41d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="41d7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d7b-111">-DefaultProfile</span></span>
<span data-ttu-id="41d7b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41d7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d7b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="41d7b-113">-Force</span></span>
<span data-ttu-id="41d7b-114">當設定為 true 時，執行將不要求確認。</span><span class="sxs-lookup"><span data-stu-id="41d7b-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="41d7b-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="41d7b-115">-IncludeSubFolders</span></span>
<span data-ttu-id="41d7b-116">當設定為 true 時，會包含子資料夾中的工件。</span><span class="sxs-lookup"><span data-stu-id="41d7b-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="41d7b-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="41d7b-117">-InputPath</span></span>
<span data-ttu-id="41d7b-118">磁片上藍圖 JSON 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="41d7b-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="41d7b-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="41d7b-119">-ManagementGroupId</span></span>
<span data-ttu-id="41d7b-120">已儲存藍圖定義或將要儲存的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="41d7b-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="41d7b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="41d7b-121">-Name</span></span>
<span data-ttu-id="41d7b-122">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="41d7b-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="41d7b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d7b-123">-PassThru</span></span>
<span data-ttu-id="41d7b-124">設定之後，Cmdlet 會傳回代表已匯入藍圖定義的物件。</span><span class="sxs-lookup"><span data-stu-id="41d7b-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="41d7b-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="41d7b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41d7b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41d7b-126">-SubscriptionId</span></span>
<span data-ttu-id="41d7b-127">藍圖定義或將要儲存的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="41d7b-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="41d7b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="41d7b-128">-Confirm</span></span>
<span data-ttu-id="41d7b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41d7b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d7b-130">-WhatIf</span></span>
<span data-ttu-id="41d7b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41d7b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d7b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d7b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d7b-133">CommonParameters</span></span>
<span data-ttu-id="41d7b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41d7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d7b-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41d7b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d7b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="41d7b-136">INPUTS</span></span>

### <span data-ttu-id="41d7b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="41d7b-137">System.String</span></span>

## <span data-ttu-id="41d7b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="41d7b-138">OUTPUTS</span></span>

### <span data-ttu-id="41d7b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="41d7b-139">System.String</span></span>

## <span data-ttu-id="41d7b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="41d7b-140">NOTES</span></span>

## <span data-ttu-id="41d7b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="41d7b-141">RELATED LINKS</span></span>
