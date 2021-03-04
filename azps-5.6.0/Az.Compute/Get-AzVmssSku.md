---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: b89bf343c1737080867bbe5e8cb5397fd52f6a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902122"
---
# <span data-ttu-id="5e1a2-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="5e1a2-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="5e1a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1a2-103">為 VMSS 獲得可用的 SKUS。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="5e1a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e1a2-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e1a2-105">描述</span><span class="sxs-lookup"><span data-stu-id="5e1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1a2-106">**Get-Az VmssSku** Cmdlet 會取得虛擬機器縮放集的可用 SKU (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5e1a2-107">例子</span><span class="sxs-lookup"><span data-stu-id="5e1a2-107">EXAMPLES</span></span>

### <span data-ttu-id="5e1a2-108">範例 1：從 VMSS 取得所有可用的 SKUS</span><span class="sxs-lookup"><span data-stu-id="5e1a2-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="5e1a2-109">此命令會從名稱為 Contoso VMSS 的 VMSS 中，獲得所有屬於 ContosoGroup 資源群組的可用 SKUS。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="5e1a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e1a2-110">PARAMETERS</span></span>

### <span data-ttu-id="5e1a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1a2-111">-DefaultProfile</span></span>
<span data-ttu-id="5e1a2-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e1a2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1a2-113">-ResourceGroupName</span></span>
<span data-ttu-id="5e1a2-114">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5e1a2-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5e1a2-115">-VMScaleSetName</span></span>
<span data-ttu-id="5e1a2-116">為 VMSS 的名稱命名。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="5e1a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1a2-117">CommonParameters</span></span>
<span data-ttu-id="5e1a2-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e1a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1a2-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e1a2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1a2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5e1a2-120">INPUTS</span></span>

### <span data-ttu-id="5e1a2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5e1a2-121">System.String</span></span>

## <span data-ttu-id="5e1a2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5e1a2-122">OUTPUTS</span></span>

### <span data-ttu-id="5e1a2-123">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="5e1a2-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="5e1a2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5e1a2-124">NOTES</span></span>

## <span data-ttu-id="5e1a2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e1a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e1a2-126">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="5e1a2-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


