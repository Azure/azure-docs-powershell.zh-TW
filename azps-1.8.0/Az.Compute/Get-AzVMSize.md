---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 2ac1e336161d4cfad1bbef37ec98716456a8143c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622783"
---
# <span data-ttu-id="f1e4c-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="f1e4c-101">Get-AzVMSize</span></span>

## <span data-ttu-id="f1e4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e4c-103">取得可用的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="f1e4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1e4c-104">SYNTAX</span></span>

### <span data-ttu-id="f1e4c-105">ListVirtualMachineSizeParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f1e4c-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1e4c-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f1e4c-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1e4c-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1e4c-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1e4c-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e4c-109">**AzVMSize** Cmdlet 會取得可用的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="f1e4c-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1e4c-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e4c-111">範例1：取得位置的虛擬電腦大小</span><span class="sxs-lookup"><span data-stu-id="f1e4c-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="f1e4c-112">這個命令會取得指定位置中虛擬機器的可用大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="f1e4c-113">範例2：取得可用性集的大小</span><span class="sxs-lookup"><span data-stu-id="f1e4c-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="f1e4c-114">這個命令會針對您可以在名為 AvailabilitySet17 的可用性集中部署的虛擬機器，取得可用的大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="f1e4c-115">範例3：取得現有虛擬機器的大小</span><span class="sxs-lookup"><span data-stu-id="f1e4c-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="f1e4c-116">這個命令會取得名為 VirtualMachine12 的現有虛擬機器的可用大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="f1e4c-117">您可以將此虛擬機器的大小調整為此命令所取得的大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="f1e4c-118">參數</span><span class="sxs-lookup"><span data-stu-id="f1e4c-118">PARAMETERS</span></span>

### <span data-ttu-id="f1e4c-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="f1e4c-119">-AvailabilitySetName</span></span>
<span data-ttu-id="f1e4c-120">指定此 Cmdlet 取得可用虛擬機器大小的可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e4c-121">-DefaultProfile</span></span>
<span data-ttu-id="f1e4c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e4c-123">-位置</span><span class="sxs-lookup"><span data-stu-id="f1e4c-123">-Location</span></span>
<span data-ttu-id="f1e4c-124">指定此 Cmdlet 取得可用虛擬機器大小的位置。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f1e4c-126">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4c-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="f1e4c-127">-VMName</span></span>
<span data-ttu-id="f1e4c-128">指定虛擬機器的名稱，這個 Cmdlet 會取得可用的虛擬電腦大小來調整大小。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e4c-129">CommonParameters</span></span>
<span data-ttu-id="f1e4c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e4c-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1e4c-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e4c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f1e4c-132">INPUTS</span></span>

### <span data-ttu-id="f1e4c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f1e4c-133">System.String</span></span>

## <span data-ttu-id="f1e4c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f1e4c-134">OUTPUTS</span></span>

### <span data-ttu-id="f1e4c-135">PSVirtualMachineSize 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f1e4c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="f1e4c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f1e4c-136">NOTES</span></span>

## <span data-ttu-id="f1e4c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1e4c-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1e4c-138">AzVM</span><span class="sxs-lookup"><span data-stu-id="f1e4c-138">Get-AzVM</span></span>](./Get-AzVM.md)

