---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: b669d415e88c16f7ddfe532f05bc754561b7ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909161"
---
# <span data-ttu-id="d457b-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="d457b-101">Get-AzVMSize</span></span>

## <span data-ttu-id="d457b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d457b-102">SYNOPSIS</span></span>
<span data-ttu-id="d457b-103">獲得可用的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="d457b-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="d457b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d457b-104">SYNTAX</span></span>

### <span data-ttu-id="d457b-105">ListVirtualMachineSizeParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d457b-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d457b-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d457b-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d457b-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d457b-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d457b-108">描述</span><span class="sxs-lookup"><span data-stu-id="d457b-108">DESCRIPTION</span></span>
<span data-ttu-id="d457b-109">**Get-Az VIRTUALSize** Cmdlet 會取得可用的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="d457b-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="d457b-110">例子</span><span class="sxs-lookup"><span data-stu-id="d457b-110">EXAMPLES</span></span>

### <span data-ttu-id="d457b-111">範例 1：取得位置的虛擬機器大小</span><span class="sxs-lookup"><span data-stu-id="d457b-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="d457b-112">此命令會獲得指定位置中虛擬機器的可用大小。</span><span class="sxs-lookup"><span data-stu-id="d457b-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="d457b-113">範例 2：取得可用性集的大小</span><span class="sxs-lookup"><span data-stu-id="d457b-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="d457b-114">此命令會針對虛擬機器提供可用大小，您可以在名稱為 AvailabilitySet17 的可用性集部署。</span><span class="sxs-lookup"><span data-stu-id="d457b-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="d457b-115">範例 3：取得現有虛擬機器的大小</span><span class="sxs-lookup"><span data-stu-id="d457b-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="d457b-116">此命令會針對名為 VirtualMachine12 的現有虛擬機器提供可用大小。</span><span class="sxs-lookup"><span data-stu-id="d457b-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="d457b-117">您可以將此虛擬機器的大小調整為此命令獲得的大小。</span><span class="sxs-lookup"><span data-stu-id="d457b-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="d457b-118">參數</span><span class="sxs-lookup"><span data-stu-id="d457b-118">PARAMETERS</span></span>

### <span data-ttu-id="d457b-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d457b-119">-AvailabilitySetName</span></span>
<span data-ttu-id="d457b-120">指定此 Cmdlet 可得到可用虛擬機器大小的可用集名稱。</span><span class="sxs-lookup"><span data-stu-id="d457b-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="d457b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d457b-121">-DefaultProfile</span></span>
<span data-ttu-id="d457b-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d457b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d457b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="d457b-123">-Location</span></span>
<span data-ttu-id="d457b-124">指定此 Cmdlet 可得到可用虛擬機器大小的位置。</span><span class="sxs-lookup"><span data-stu-id="d457b-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="d457b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d457b-125">-ResourceGroupName</span></span>
<span data-ttu-id="d457b-126">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d457b-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d457b-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="d457b-127">-VMName</span></span>
<span data-ttu-id="d457b-128">指定此 Cmdlet 可調整可用虛擬機器大小的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d457b-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="d457b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d457b-129">CommonParameters</span></span>
<span data-ttu-id="d457b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d457b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d457b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d457b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d457b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d457b-132">INPUTS</span></span>

### <span data-ttu-id="d457b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d457b-133">System.String</span></span>

## <span data-ttu-id="d457b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d457b-134">OUTPUTS</span></span>

### <span data-ttu-id="d457b-135">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="d457b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="d457b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d457b-136">NOTES</span></span>

## <span data-ttu-id="d457b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d457b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d457b-138">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="d457b-138">Get-AzVM</span></span>](./Get-AzVM.md)


