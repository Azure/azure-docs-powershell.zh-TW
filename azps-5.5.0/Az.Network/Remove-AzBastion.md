---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140282"
---
# <span data-ttu-id="f2c43-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="f2c43-101">Remove-AzBastion</span></span>

## <span data-ttu-id="f2c43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2c43-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c43-103">移除堡壘資源。</span><span class="sxs-lookup"><span data-stu-id="f2c43-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="f2c43-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2c43-104">SYNTAX</span></span>

### <span data-ttu-id="f2c43-105">ByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="f2c43-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2c43-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2c43-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2c43-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2c43-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2c43-108">說明</span><span class="sxs-lookup"><span data-stu-id="f2c43-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c43-109">移除堡壘資源。Example1 會使用其 ResourceGroupName 和 CoNtext.resourcename 來刪除堡壘。</span><span class="sxs-lookup"><span data-stu-id="f2c43-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="f2c43-110">Example2 會將堡壘使用其物件與管線一起刪除。</span><span class="sxs-lookup"><span data-stu-id="f2c43-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="f2c43-111">Example3 會使用其物件刪除堡壘。</span><span class="sxs-lookup"><span data-stu-id="f2c43-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="f2c43-112">示例</span><span class="sxs-lookup"><span data-stu-id="f2c43-112">EXAMPLES</span></span>

### <span data-ttu-id="f2c43-113">範例1</span><span class="sxs-lookup"><span data-stu-id="f2c43-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="f2c43-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f2c43-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="f2c43-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f2c43-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="f2c43-116">參數</span><span class="sxs-lookup"><span data-stu-id="f2c43-116">PARAMETERS</span></span>

### <span data-ttu-id="f2c43-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f2c43-117">-Confirm</span></span>
<span data-ttu-id="f2c43-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2c43-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c43-119">-DefaultProfile</span></span>
<span data-ttu-id="f2c43-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2c43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2c43-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f2c43-121">-Force</span></span>
<span data-ttu-id="f2c43-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f2c43-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2c43-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2c43-123">-InputObject</span></span>
<span data-ttu-id="f2c43-124">要刪除的堡壘物件。</span><span class="sxs-lookup"><span data-stu-id="f2c43-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2c43-125">-Name</span></span>
<span data-ttu-id="f2c43-126">要刪除的堡壘資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f2c43-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2c43-127">-PassThru</span></span>
<span data-ttu-id="f2c43-128">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f2c43-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="f2c43-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c43-129">-ResourceGroupName</span></span>
<span data-ttu-id="f2c43-130">堡壘存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2c43-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2c43-131">-ResourceId</span></span>
<span data-ttu-id="f2c43-132">要刪除之堡壘的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2c43-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2c43-133">-WhatIf</span></span>
<span data-ttu-id="f2c43-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2c43-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2c43-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2c43-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c43-136">CommonParameters</span></span>
<span data-ttu-id="f2c43-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2c43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c43-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2c43-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c43-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f2c43-139">INPUTS</span></span>

### <span data-ttu-id="f2c43-140">PSBastion 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2c43-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="f2c43-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f2c43-141">System.String</span></span>

## <span data-ttu-id="f2c43-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f2c43-142">OUTPUTS</span></span>

### <span data-ttu-id="f2c43-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f2c43-143">System.Boolean</span></span>

## <span data-ttu-id="f2c43-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f2c43-144">NOTES</span></span>

## <span data-ttu-id="f2c43-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2c43-145">RELATED LINKS</span></span>
[<span data-ttu-id="f2c43-146">AzBastion</span><span class="sxs-lookup"><span data-stu-id="f2c43-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="f2c43-147">新-AzBastion</span><span class="sxs-lookup"><span data-stu-id="f2c43-147">New-AzBastion</span></span>](./New-AzBastion.md)