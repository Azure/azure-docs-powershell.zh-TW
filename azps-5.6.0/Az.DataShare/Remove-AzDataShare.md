---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905105"
---
# <span data-ttu-id="31f37-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="31f37-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="31f37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31f37-102">SYNOPSIS</span></span>
<span data-ttu-id="31f37-103">移除資料共用。</span><span class="sxs-lookup"><span data-stu-id="31f37-103">Removes a data share.</span></span>

## <span data-ttu-id="31f37-104">語法</span><span class="sxs-lookup"><span data-stu-id="31f37-104">SYNTAX</span></span>

### <span data-ttu-id="31f37-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="31f37-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f37-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f37-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f37-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f37-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f37-108">描述</span><span class="sxs-lookup"><span data-stu-id="31f37-108">DESCRIPTION</span></span>
<span data-ttu-id="31f37-109">**Remove-AzDataShare** Cmdlet 會移除資料共用。</span><span class="sxs-lookup"><span data-stu-id="31f37-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="31f37-110">例子</span><span class="sxs-lookup"><span data-stu-id="31f37-110">EXAMPLES</span></span>

### <span data-ttu-id="31f37-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="31f37-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="31f37-112">這個命令會從 Azure 資料共用帳戶 WikiAds 移除名為 AdsShare 的資料共用。</span><span class="sxs-lookup"><span data-stu-id="31f37-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="31f37-113">參數</span><span class="sxs-lookup"><span data-stu-id="31f37-113">PARAMETERS</span></span>

### <span data-ttu-id="31f37-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31f37-114">-AccountName</span></span>
<span data-ttu-id="31f37-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="31f37-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f37-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31f37-116">-AsJob</span></span>
<span data-ttu-id="31f37-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="31f37-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="31f37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f37-118">-DefaultProfile</span></span>
<span data-ttu-id="31f37-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31f37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f37-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31f37-120">-InputObject</span></span>
<span data-ttu-id="31f37-121">Azure 資料共用物件''yaml 類型：PSDataShare 參數集：ByObjectParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="31f37-122">需要：True Position：已命名的預設值：無接受管線輸入：True (ByValue) 接受萬用字元： False</span><span class="sxs-lookup"><span data-stu-id="31f37-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31f37-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="31f37-123">-Name</span></span>
<span data-ttu-id="31f37-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="31f37-124">Azure data share name</span></span>

<span data-ttu-id="31f37-125">yaml 類型：字串參數集：ByFieldsParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="31f37-126">需要：True Position：已命名的預設值：無接受管線輸入：False Accept 萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f37-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31f37-127">-PassThru</span></span>
<span data-ttu-id="31f37-128">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="31f37-128">Return object (if specified).</span></span>

<span data-ttu-id="31f37-129">yaml 類型：SwitchParameter 參數集： (所有) 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="31f37-130">需要：False Position：已命名的預設值：無接受管線輸入：False Accept 萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="31f37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f37-131">-ResourceGroupName</span></span>
<span data-ttu-id="31f37-132">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="31f37-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="31f37-133">yaml 類型：字串參數集：ByFieldsParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="31f37-134">需要：True Position：已命名的預設值：無接受管線輸入：False Accept 萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f37-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31f37-135">-ResourceId</span></span>
<span data-ttu-id="31f37-136">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="31f37-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="31f37-137">yaml 類型：字串參數集：ByResourceIdParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="31f37-138">需要：True Position：已命名的預設值：無接受管線輸入：True (ByPropertyName) 接受萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f37-139">-確認</span><span class="sxs-lookup"><span data-stu-id="31f37-139">-Confirm</span></span>
<span data-ttu-id="31f37-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31f37-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="31f37-141">yaml 類型：SwitchParameter 參數集： (所有) 別名：cf</span><span class="sxs-lookup"><span data-stu-id="31f37-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="31f37-142">需要：False Position：已命名的預設值：無接受管線輸入：False Accept 萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="31f37-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f37-143">-WhatIf</span></span>
<span data-ttu-id="31f37-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31f37-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f37-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31f37-145">The cmdlet is not run.</span></span>

<span data-ttu-id="31f37-146">yaml 類型：SwitchParameter 參數集： (所有) 別名：wi</span><span class="sxs-lookup"><span data-stu-id="31f37-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="31f37-147">需要：False Position：已命名的預設值：無接受管線輸入：False Accept 萬用字元：False</span><span class="sxs-lookup"><span data-stu-id="31f37-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="31f37-148">yaml 類型：Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 參數集：ByObjectParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="31f37-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="31f37-149">需要：True Position：已命名的預設值：無接受管線輸入：True (ByValue) 接受萬用字元： False</span><span class="sxs-lookup"><span data-stu-id="31f37-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="31f37-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f37-150">CommonParameters</span></span>
<span data-ttu-id="31f37-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31f37-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f37-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f37-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f37-153">輸入</span><span class="sxs-lookup"><span data-stu-id="31f37-153">INPUTS</span></span>

### <span data-ttu-id="31f37-154">System.String</span><span class="sxs-lookup"><span data-stu-id="31f37-154">System.String</span></span>

### <span data-ttu-id="31f37-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="31f37-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="31f37-156">輸出</span><span class="sxs-lookup"><span data-stu-id="31f37-156">OUTPUTS</span></span>

### <span data-ttu-id="31f37-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31f37-157">System.Boolean</span></span>

## <span data-ttu-id="31f37-158">筆記</span><span class="sxs-lookup"><span data-stu-id="31f37-158">NOTES</span></span>

## <span data-ttu-id="31f37-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="31f37-159">RELATED LINKS</span></span>
