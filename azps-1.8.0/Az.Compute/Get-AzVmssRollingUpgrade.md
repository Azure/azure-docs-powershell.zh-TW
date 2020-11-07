---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788478"
---
# <span data-ttu-id="91be3-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="91be3-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="91be3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91be3-102">SYNOPSIS</span></span>
<span data-ttu-id="91be3-103">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="91be3-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="91be3-104">句法</span><span class="sxs-lookup"><span data-stu-id="91be3-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91be3-105">說明</span><span class="sxs-lookup"><span data-stu-id="91be3-105">DESCRIPTION</span></span>
<span data-ttu-id="91be3-106">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="91be3-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="91be3-107">示例</span><span class="sxs-lookup"><span data-stu-id="91be3-107">EXAMPLES</span></span>

### <span data-ttu-id="91be3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="91be3-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="91be3-109">這個命令會顯示屬於名為 Group001 之資源群組之名為 VMSS001 之 VMSS 的最新輪流升級狀態。</span><span class="sxs-lookup"><span data-stu-id="91be3-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="91be3-110">參數</span><span class="sxs-lookup"><span data-stu-id="91be3-110">PARAMETERS</span></span>

### <span data-ttu-id="91be3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91be3-111">-DefaultProfile</span></span>
<span data-ttu-id="91be3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91be3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91be3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91be3-113">-ResourceGroupName</span></span>
<span data-ttu-id="91be3-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91be3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="91be3-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="91be3-115">-VMScaleSetName</span></span>
<span data-ttu-id="91be3-116">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="91be3-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="91be3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91be3-117">CommonParameters</span></span>
<span data-ttu-id="91be3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91be3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91be3-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="91be3-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91be3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="91be3-120">INPUTS</span></span>

### <span data-ttu-id="91be3-121">System.object</span><span class="sxs-lookup"><span data-stu-id="91be3-121">System.String</span></span>

## <span data-ttu-id="91be3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="91be3-122">OUTPUTS</span></span>

### <span data-ttu-id="91be3-123">PSRollingUpgradeStatusInfo 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="91be3-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="91be3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="91be3-124">NOTES</span></span>

## <span data-ttu-id="91be3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="91be3-125">RELATED LINKS</span></span>
