---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914901"
---
# <span data-ttu-id="63184-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="63184-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="63184-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63184-102">SYNOPSIS</span></span>
<span data-ttu-id="63184-103">獲得 VMSS 虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="63184-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="63184-104">語法</span><span class="sxs-lookup"><span data-stu-id="63184-104">SYNTAX</span></span>

### <span data-ttu-id="63184-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="63184-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63184-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="63184-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63184-107">描述</span><span class="sxs-lookup"><span data-stu-id="63184-107">DESCRIPTION</span></span>
<span data-ttu-id="63184-108">**Get-Az Vmss VM Cmdlet** 會取得虛擬機器的虛擬機器縮放集模型 (VMSS) 實例視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="63184-109">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="63184-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="63184-110">實例視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="63184-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="63184-111">指定 *狀態* 參數以僅取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="63184-112">例子</span><span class="sxs-lookup"><span data-stu-id="63184-112">EXAMPLES</span></span>

### <span data-ttu-id="63184-113">範例 1：取得 VMSS 虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="63184-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="63184-114">此命令會獲得名為 VMSS001 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="63184-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="63184-115">由於命令未指定 *InstanceView* 參數，因此 Cmdlet 會獲得虛擬機器的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="63184-116">範例 2：取得 VMSS 虛擬機器的模型視圖屬性</span><span class="sxs-lookup"><span data-stu-id="63184-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="63184-117">此命令會獲得名為 VMSS004 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="63184-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="63184-118">該命令會取得儲存在變數中的實例識別碼$ID取得模型視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="63184-119">範例 3：取得 VMSS 虛擬機器的實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="63184-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="63184-120">此命令會獲得名為 VMSS004 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="63184-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="63184-121">由於命令指定 *InstanceView* 參數，因此 Cmdlet 會獲得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="63184-122">該命令會取得儲存在變數中的實例識別碼$ID取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="63184-123">參數</span><span class="sxs-lookup"><span data-stu-id="63184-123">PARAMETERS</span></span>

### <span data-ttu-id="63184-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63184-124">-DefaultProfile</span></span>
<span data-ttu-id="63184-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63184-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63184-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="63184-126">-InstanceId</span></span>
<span data-ttu-id="63184-127">指定取得模型視圖的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="63184-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63184-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="63184-128">-InstanceView</span></span>
<span data-ttu-id="63184-129">表示此 Cmdlet 僅會獲得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="63184-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="63184-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63184-130">-ResourceGroupName</span></span>
<span data-ttu-id="63184-131">指定 VMSS 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="63184-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63184-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="63184-132">-VMScaleSetName</span></span>
<span data-ttu-id="63184-133">為 VMSS 的名稱命名。</span><span class="sxs-lookup"><span data-stu-id="63184-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63184-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63184-134">CommonParameters</span></span>
<span data-ttu-id="63184-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63184-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63184-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63184-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63184-137">輸入</span><span class="sxs-lookup"><span data-stu-id="63184-137">INPUTS</span></span>

### <span data-ttu-id="63184-138">System.String</span><span class="sxs-lookup"><span data-stu-id="63184-138">System.String</span></span>

## <span data-ttu-id="63184-139">輸出</span><span class="sxs-lookup"><span data-stu-id="63184-139">OUTPUTS</span></span>

### <span data-ttu-id="63184-140">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="63184-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="63184-141">筆記</span><span class="sxs-lookup"><span data-stu-id="63184-141">NOTES</span></span>

## <span data-ttu-id="63184-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="63184-142">RELATED LINKS</span></span>

[<span data-ttu-id="63184-143">Set-AzEvssVM</span><span class="sxs-lookup"><span data-stu-id="63184-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="63184-144">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="63184-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


