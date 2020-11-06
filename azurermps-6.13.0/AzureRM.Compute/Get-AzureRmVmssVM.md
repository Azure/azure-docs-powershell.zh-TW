---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 00325dc33daa6ec58693dbe6cd6d526ac41b8fd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453860"
---
# <span data-ttu-id="2f4ea-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="2f4ea-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="2f4ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4ea-103">取得 VMSS 虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f4ea-104">SYNTAX</span></span>

### <span data-ttu-id="2f4ea-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2f4ea-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f4ea-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2f4ea-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f4ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4ea-108">**AzureRmVmssVM** Cmdlet 會取得虛擬機器規模集的模型視圖和實例視圖， (VMSS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="2f4ea-109">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="2f4ea-110">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="2f4ea-111">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="2f4ea-112">示例</span><span class="sxs-lookup"><span data-stu-id="2f4ea-112">EXAMPLES</span></span>

### <span data-ttu-id="2f4ea-113">範例1：取得 VMSS 虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="2f4ea-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="2f4ea-114">這個命令會取得名為 VMSS001 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="2f4ea-115">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="2f4ea-116">範例2：取得 VMSS 虛擬機器的模型視圖屬性</span><span class="sxs-lookup"><span data-stu-id="2f4ea-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="2f4ea-117">這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="2f4ea-118">命令會取得儲存在變數 $ID 中的實例識別碼，以取得模型視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="2f4ea-119">範例3：取得 VMSS 虛擬機器的實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="2f4ea-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="2f4ea-120">這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="2f4ea-121">由於命令會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="2f4ea-122">命令會取得儲存在變數 $ID 中的實例識別碼，以取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="2f4ea-123">參數</span><span class="sxs-lookup"><span data-stu-id="2f4ea-123">PARAMETERS</span></span>

### <span data-ttu-id="2f4ea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4ea-124">-DefaultProfile</span></span>
<span data-ttu-id="2f4ea-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f4ea-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2f4ea-126">-InstanceId</span></span>
<span data-ttu-id="2f4ea-127">指定要取得模型視圖的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4ea-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="2f4ea-128">-InstanceView</span></span>
<span data-ttu-id="2f4ea-129">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="2f4ea-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4ea-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2f4ea-132">-VMScaleSetName</span></span>
<span data-ttu-id="2f4ea-133">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4ea-134">CommonParameters</span></span>
<span data-ttu-id="2f4ea-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4ea-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4ea-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2f4ea-137">INPUTS</span></span>

### <span data-ttu-id="2f4ea-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2f4ea-138">System.String</span></span>

## <span data-ttu-id="2f4ea-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2f4ea-139">OUTPUTS</span></span>

### <span data-ttu-id="2f4ea-140">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2f4ea-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2f4ea-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2f4ea-141">NOTES</span></span>

## <span data-ttu-id="2f4ea-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f4ea-142">RELATED LINKS</span></span>

[<span data-ttu-id="2f4ea-143">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="2f4ea-143">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="2f4ea-144">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2f4ea-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


