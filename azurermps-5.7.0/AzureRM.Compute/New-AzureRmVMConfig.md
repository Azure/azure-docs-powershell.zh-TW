---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 45cb93e652f9c1524ef1bb11972f184336ef7328
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624198"
---
# <span data-ttu-id="b05a2-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b05a2-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="b05a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b05a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b05a2-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="b05a2-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b05a2-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [-LicenseType <String>] [-IdentityType <ResourceIdentityType>] [-Tags <Hashtable>] [<CommonParameters>]
```

## <span data-ttu-id="b05a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="b05a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b05a2-106">**新的-AzureRmVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="b05a2-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="b05a2-107">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="b05a2-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="b05a2-108">示例</span><span class="sxs-lookup"><span data-stu-id="b05a2-108">EXAMPLES</span></span>

### <span data-ttu-id="b05a2-109">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="b05a2-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="b05a2-110">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="b05a2-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="b05a2-111">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="b05a2-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b05a2-112">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b05a2-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b05a2-113">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="b05a2-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="b05a2-114">參數</span><span class="sxs-lookup"><span data-stu-id="b05a2-114">PARAMETERS</span></span>

### <span data-ttu-id="b05a2-115">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="b05a2-115">-AvailabilitySetId</span></span>
<span data-ttu-id="b05a2-116">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="b05a2-116">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="b05a2-117">若要取得可用性集物件，請使用 Get-AzureRmAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b05a2-117">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="b05a2-118">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="b05a2-118">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a2-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b05a2-119">-IdentityType</span></span>
<span data-ttu-id="b05a2-120">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="b05a2-120">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05a2-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b05a2-121">-LicenseType</span></span>
<span data-ttu-id="b05a2-122">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="b05a2-122">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05a2-123">-標記</span><span class="sxs-lookup"><span data-stu-id="b05a2-123">-Tags</span></span>
<span data-ttu-id="b05a2-124">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="b05a2-124">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a2-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b05a2-125">-VMName</span></span>
<span data-ttu-id="b05a2-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b05a2-126">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a2-127">-VMSize</span><span class="sxs-lookup"><span data-stu-id="b05a2-127">-VMSize</span></span>
<span data-ttu-id="b05a2-128">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="b05a2-128">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="b05a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05a2-129">CommonParameters</span></span>
<span data-ttu-id="b05a2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b05a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05a2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b05a2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05a2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b05a2-132">INPUTS</span></span>

### <span data-ttu-id="b05a2-133">所有</span><span class="sxs-lookup"><span data-stu-id="b05a2-133">None</span></span>
<span data-ttu-id="b05a2-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b05a2-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b05a2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b05a2-135">OUTPUTS</span></span>

## <span data-ttu-id="b05a2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b05a2-136">NOTES</span></span>

## <span data-ttu-id="b05a2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b05a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="b05a2-138">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b05a2-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="b05a2-139">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b05a2-139">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="b05a2-140">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="b05a2-140">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="b05a2-141">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b05a2-141">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


