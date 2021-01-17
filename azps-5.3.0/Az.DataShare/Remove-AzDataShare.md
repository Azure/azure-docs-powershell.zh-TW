---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286356"
---
# <span data-ttu-id="fd9df-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="fd9df-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="fd9df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd9df-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9df-103">移除資料共用。</span><span class="sxs-lookup"><span data-stu-id="fd9df-103">Removes a data share.</span></span>

## <span data-ttu-id="fd9df-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd9df-104">SYNTAX</span></span>

### <span data-ttu-id="fd9df-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fd9df-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9df-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9df-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9df-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9df-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd9df-108">說明</span><span class="sxs-lookup"><span data-stu-id="fd9df-108">DESCRIPTION</span></span>
<span data-ttu-id="fd9df-109">**AzDataShare** Cmdlet 會移除資料共用。</span><span class="sxs-lookup"><span data-stu-id="fd9df-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="fd9df-110">示例</span><span class="sxs-lookup"><span data-stu-id="fd9df-110">EXAMPLES</span></span>

### <span data-ttu-id="fd9df-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fd9df-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="fd9df-112">這個命令會從 azure 資料共用帳戶 WikiAds 中移除名為 AdsShare 的資料共用。</span><span class="sxs-lookup"><span data-stu-id="fd9df-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="fd9df-113">參數</span><span class="sxs-lookup"><span data-stu-id="fd9df-113">PARAMETERS</span></span>

### <span data-ttu-id="fd9df-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd9df-114">-AccountName</span></span>
<span data-ttu-id="fd9df-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="fd9df-115">Azure data share account name</span></span>

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

### <span data-ttu-id="fd9df-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd9df-116">-AsJob</span></span>
<span data-ttu-id="fd9df-117">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="fd9df-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="fd9df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9df-118">-DefaultProfile</span></span>
<span data-ttu-id="fd9df-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd9df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd9df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd9df-120">-InputObject</span></span>
<span data-ttu-id="fd9df-121">Azure data share 物件 "" yaml 類型： PSDataShare 參數集： ByObjectParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="fd9df-122">必要： True 位置：命名的預設值： None 接受管線輸入： True (ByValue) 接受萬用字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd9df-123">-Name</span></span>
<span data-ttu-id="fd9df-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="fd9df-124">Azure data share name</span></span>

<span data-ttu-id="fd9df-125">yaml 類型：字串參數集： ByFieldsParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="fd9df-126">必要： True 位置：命名的預設值： None 接受管線輸入： False 接受通配字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd9df-127">-PassThru</span></span>
<span data-ttu-id="fd9df-128">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="fd9df-128">Return object (if specified).</span></span>

<span data-ttu-id="fd9df-129">yaml 類型： SwitchParameter 參數集： (所有) 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="fd9df-130">必要： False 位置：命名的預設值： None [接受管線] 輸入： False 接受通配字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9df-131">-ResourceGroupName</span></span>
<span data-ttu-id="fd9df-132">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="fd9df-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="fd9df-133">yaml 類型：字串參數集： ByFieldsParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="fd9df-134">必要： True 位置：命名的預設值： None 接受管線輸入： False 接受通配字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd9df-135">-ResourceId</span></span>
<span data-ttu-id="fd9df-136">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd9df-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="fd9df-137">yaml 類型：字串參數集： ByResourceIdParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="fd9df-138">必要： True 位置：命名的預設值： None 接受管線輸入： True (ByPropertyName) 接受萬用字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-139">-確認</span><span class="sxs-lookup"><span data-stu-id="fd9df-139">-Confirm</span></span>
<span data-ttu-id="fd9df-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fd9df-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="fd9df-141">yaml 類型： SwitchParameter 參數集： (所有) 別名： cf</span><span class="sxs-lookup"><span data-stu-id="fd9df-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="fd9df-142">必要： False 位置：命名的預設值： None [接受管線] 輸入： False 接受通配字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9df-143">-WhatIf</span></span>
<span data-ttu-id="fd9df-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd9df-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd9df-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd9df-145">The cmdlet is not run.</span></span>

<span data-ttu-id="fd9df-146">yaml 類型： SwitchParameter 參數集： (所有) 別名： wi</span><span class="sxs-lookup"><span data-stu-id="fd9df-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="fd9df-147">必要： False 位置：命名的預設值： None [接受管線] 輸入： False 接受通配字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="fd9df-148">yaml 類型： Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 參數集： ByObjectParameterSet 別名：</span><span class="sxs-lookup"><span data-stu-id="fd9df-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="fd9df-149">必要： True 位置：命名的預設值： None 接受管線輸入： True (ByValue) 接受萬用字元： False</span><span class="sxs-lookup"><span data-stu-id="fd9df-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="fd9df-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9df-150">CommonParameters</span></span>
<span data-ttu-id="fd9df-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd9df-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9df-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fd9df-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9df-153">輸入</span><span class="sxs-lookup"><span data-stu-id="fd9df-153">INPUTS</span></span>

### <span data-ttu-id="fd9df-154">System.object</span><span class="sxs-lookup"><span data-stu-id="fd9df-154">System.String</span></span>

### <span data-ttu-id="fd9df-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="fd9df-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="fd9df-156">輸出</span><span class="sxs-lookup"><span data-stu-id="fd9df-156">OUTPUTS</span></span>

### <span data-ttu-id="fd9df-157">System.object</span><span class="sxs-lookup"><span data-stu-id="fd9df-157">System.Boolean</span></span>

## <span data-ttu-id="fd9df-158">筆記</span><span class="sxs-lookup"><span data-stu-id="fd9df-158">NOTES</span></span>

## <span data-ttu-id="fd9df-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd9df-159">RELATED LINKS</span></span>
