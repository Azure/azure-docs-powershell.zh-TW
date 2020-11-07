---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef9d1ac2e5bca51ee1addf8fdffd87c5045d23eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625920"
---
# <span data-ttu-id="f2d76-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f2d76-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="f2d76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2d76-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d76-103">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="f2d76-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d76-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2d76-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2d76-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2d76-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d76-106">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="f2d76-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f2d76-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2d76-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d76-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f2d76-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f2d76-109">這個命令會顯示屬於名為 Group001 之資源群組之名為 VMSS001 之 VMSS 的最新輪流升級狀態。</span><span class="sxs-lookup"><span data-stu-id="f2d76-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f2d76-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2d76-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d76-111">-DefaultProfile</span></span>
<span data-ttu-id="f2d76-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2d76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d76-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d76-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2d76-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2d76-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d76-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2d76-115">-VMScaleSetName</span></span>
<span data-ttu-id="f2d76-116">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2d76-116">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d76-117">CommonParameters</span></span>
<span data-ttu-id="f2d76-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2d76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d76-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2d76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d76-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f2d76-120">INPUTS</span></span>

### <span data-ttu-id="f2d76-121">System.object</span><span class="sxs-lookup"><span data-stu-id="f2d76-121">System.String</span></span>

## <span data-ttu-id="f2d76-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f2d76-122">OUTPUTS</span></span>

### <span data-ttu-id="f2d76-123">PSRollingUpgradeStatusInfo 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f2d76-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="f2d76-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f2d76-124">NOTES</span></span>

## <span data-ttu-id="f2d76-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2d76-125">RELATED LINKS</span></span>
