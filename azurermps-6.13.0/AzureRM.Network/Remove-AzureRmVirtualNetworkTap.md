---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448307"
---
# <span data-ttu-id="ec56e-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ec56e-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="ec56e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec56e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec56e-103">移除虛擬網路攻絲。</span><span class="sxs-lookup"><span data-stu-id="ec56e-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec56e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec56e-104">SYNTAX</span></span>

### <span data-ttu-id="ec56e-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec56e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec56e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec56e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec56e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec56e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec56e-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec56e-108">DESCRIPTION</span></span>
<span data-ttu-id="ec56e-109">**AzureRmVirtualNetworkTap** Cmdlet 會移除 Azure 虛擬網路分流。</span><span class="sxs-lookup"><span data-stu-id="ec56e-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="ec56e-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec56e-110">EXAMPLES</span></span>

### <span data-ttu-id="ec56e-111">範例1：移除 virtuak 網路攻絲</span><span class="sxs-lookup"><span data-stu-id="ec56e-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="ec56e-112">這個命令會移除資源群組 ResourceGroup1 中的 VirtualNetworkTap1。</span><span class="sxs-lookup"><span data-stu-id="ec56e-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="ec56e-113">由於不使用 *Force* 參數，系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="ec56e-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="ec56e-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec56e-114">PARAMETERS</span></span>

### <span data-ttu-id="ec56e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec56e-115">-AsJob</span></span>
<span data-ttu-id="ec56e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec56e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec56e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec56e-117">-DefaultProfile</span></span>
<span data-ttu-id="ec56e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec56e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec56e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ec56e-119">-Force</span></span>
<span data-ttu-id="ec56e-120">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ec56e-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ec56e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec56e-121">-InputObject</span></span>
<span data-ttu-id="ec56e-122">VirtualNetworkTap 資源的參照</span><span class="sxs-lookup"><span data-stu-id="ec56e-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec56e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec56e-123">-Name</span></span>
<span data-ttu-id="ec56e-124">攻絲的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec56e-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec56e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec56e-125">-PassThru</span></span>
<span data-ttu-id="ec56e-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ec56e-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec56e-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ec56e-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec56e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec56e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec56e-129">虛擬網路的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="ec56e-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec56e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec56e-130">-ResourceId</span></span>
<span data-ttu-id="ec56e-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="ec56e-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec56e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ec56e-132">-Confirm</span></span>
<span data-ttu-id="ec56e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec56e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec56e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec56e-134">-WhatIf</span></span>
<span data-ttu-id="ec56e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec56e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec56e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec56e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec56e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec56e-137">CommonParameters</span></span>
<span data-ttu-id="ec56e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec56e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec56e-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec56e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec56e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ec56e-140">INPUTS</span></span>

### <span data-ttu-id="ec56e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ec56e-141">System.String</span></span>

## <span data-ttu-id="ec56e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ec56e-142">OUTPUTS</span></span>

### <span data-ttu-id="ec56e-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ec56e-143">System.Boolean</span></span>

## <span data-ttu-id="ec56e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ec56e-144">NOTES</span></span>

## <span data-ttu-id="ec56e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec56e-145">RELATED LINKS</span></span>
