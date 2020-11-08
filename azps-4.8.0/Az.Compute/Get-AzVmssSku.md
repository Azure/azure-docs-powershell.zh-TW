---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971478"
---
# <span data-ttu-id="ad66d-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="ad66d-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="ad66d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad66d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad66d-103">取得 VMSS 可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="ad66d-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="ad66d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad66d-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad66d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad66d-105">DESCRIPTION</span></span>
<span data-ttu-id="ad66d-106">**AzVmssSku** Cmdlet 會取得適用于虛擬機器規模集 (VMSS) 的可用 sku。</span><span class="sxs-lookup"><span data-stu-id="ad66d-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ad66d-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad66d-107">EXAMPLES</span></span>

### <span data-ttu-id="ad66d-108">範例1：從 VMSS 取得所有可用的 Sku</span><span class="sxs-lookup"><span data-stu-id="ad66d-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ad66d-109">這個命令會從屬於名為 ContosoGroup 之資源群組的名為 ContosoVMSS 的 VMSS 中取得所有可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="ad66d-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ad66d-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad66d-110">PARAMETERS</span></span>

### <span data-ttu-id="ad66d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad66d-111">-DefaultProfile</span></span>
<span data-ttu-id="ad66d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad66d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad66d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad66d-113">-ResourceGroupName</span></span>
<span data-ttu-id="ad66d-114">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad66d-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ad66d-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ad66d-115">-VMScaleSetName</span></span>
<span data-ttu-id="ad66d-116">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad66d-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ad66d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad66d-117">CommonParameters</span></span>
<span data-ttu-id="ad66d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad66d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad66d-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad66d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad66d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ad66d-120">INPUTS</span></span>

### <span data-ttu-id="ad66d-121">System.object</span><span class="sxs-lookup"><span data-stu-id="ad66d-121">System.String</span></span>

## <span data-ttu-id="ad66d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ad66d-122">OUTPUTS</span></span>

### <span data-ttu-id="ad66d-123">PSVirtualMachineScaleSetSku 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ad66d-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="ad66d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ad66d-124">NOTES</span></span>

## <span data-ttu-id="ad66d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad66d-125">RELATED LINKS</span></span>

[<span data-ttu-id="ad66d-126">AzVmss</span><span class="sxs-lookup"><span data-stu-id="ad66d-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


