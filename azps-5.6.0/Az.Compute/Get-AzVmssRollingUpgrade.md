---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: e87c307592f4487de239245ef06a70ea084ef916
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903330"
---
# <span data-ttu-id="5a397-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a397-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="5a397-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a397-102">SYNOPSIS</span></span>
<span data-ttu-id="5a397-103">顯示最新虛擬機器規模集輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a397-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="5a397-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a397-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a397-105">描述</span><span class="sxs-lookup"><span data-stu-id="5a397-105">DESCRIPTION</span></span>
<span data-ttu-id="5a397-106">顯示最新虛擬機器規模集輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a397-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="5a397-107">例子</span><span class="sxs-lookup"><span data-stu-id="5a397-107">EXAMPLES</span></span>

### <span data-ttu-id="5a397-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a397-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="5a397-109">此命令顯示屬於 Group001 資源群組的 VMSS 名稱為 VMSS001 的最新輪流升級狀態。</span><span class="sxs-lookup"><span data-stu-id="5a397-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5a397-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a397-110">PARAMETERS</span></span>

### <span data-ttu-id="5a397-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a397-111">-DefaultProfile</span></span>
<span data-ttu-id="5a397-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a397-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a397-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a397-113">-ResourceGroupName</span></span>
<span data-ttu-id="5a397-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a397-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a397-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5a397-115">-VMScaleSetName</span></span>
<span data-ttu-id="5a397-116">VM 縮放集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a397-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="5a397-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a397-117">CommonParameters</span></span>
<span data-ttu-id="5a397-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a397-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a397-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a397-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a397-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5a397-120">INPUTS</span></span>

### <span data-ttu-id="5a397-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5a397-121">System.String</span></span>

## <span data-ttu-id="5a397-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5a397-122">OUTPUTS</span></span>

### <span data-ttu-id="5a397-123">Microsoft.Azure.Commands.Compute.Automation.models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="5a397-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="5a397-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5a397-124">NOTES</span></span>

## <span data-ttu-id="5a397-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a397-125">RELATED LINKS</span></span>
