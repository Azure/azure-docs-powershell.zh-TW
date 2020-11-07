---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625353"
---
# <span data-ttu-id="bdc35-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="bdc35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdc35-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc35-103">取得 VMSS 的屬性。</span><span class="sxs-lookup"><span data-stu-id="bdc35-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdc35-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdc35-104">SYNTAX</span></span>

### <span data-ttu-id="bdc35-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="bdc35-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdc35-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="bdc35-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdc35-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="bdc35-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdc35-108">說明</span><span class="sxs-lookup"><span data-stu-id="bdc35-108">DESCRIPTION</span></span>
<span data-ttu-id="bdc35-109">**AzureRmVmss** Cmdlet 會取得虛擬機器縮放集 (VMSS) 的模型和實例視圖。</span><span class="sxs-lookup"><span data-stu-id="bdc35-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="bdc35-110">模型視圖是使用者指定的虛擬機器規模設定屬性。</span><span class="sxs-lookup"><span data-stu-id="bdc35-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="bdc35-111">[實例] 視圖是虛擬機器規模集的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="bdc35-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="bdc35-112">指定 *InstanceView* 參數，只取得虛擬機器縮放集的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="bdc35-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="bdc35-113">示例</span><span class="sxs-lookup"><span data-stu-id="bdc35-113">EXAMPLES</span></span>

### <span data-ttu-id="bdc35-114">範例1：取得 VMSS 的屬性</span><span class="sxs-lookup"><span data-stu-id="bdc35-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="bdc35-115">這個命令會取得屬於名為 Group001 之資源群組之名為 VMSS001 的 VMSS 屬性。</span><span class="sxs-lookup"><span data-stu-id="bdc35-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="bdc35-116">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器縮放集的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="bdc35-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="bdc35-117">參數</span><span class="sxs-lookup"><span data-stu-id="bdc35-117">PARAMETERS</span></span>

### <span data-ttu-id="bdc35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc35-118">-DefaultProfile</span></span>
<span data-ttu-id="bdc35-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdc35-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc35-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="bdc35-120">-InstanceView</span></span>
<span data-ttu-id="bdc35-121">表示此 Cmdlet 只會取得虛擬機器縮放集的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="bdc35-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bdc35-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="bdc35-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="bdc35-123">表示此 Cmdlet 列出虛擬機器規模集的 os 升級歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="bdc35-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdc35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc35-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdc35-125">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdc35-125">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="bdc35-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bdc35-126">-VMScaleSetName</span></span>
<span data-ttu-id="bdc35-127">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdc35-127">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="bdc35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc35-128">CommonParameters</span></span>
<span data-ttu-id="bdc35-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdc35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc35-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bdc35-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc35-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bdc35-131">INPUTS</span></span>

### <span data-ttu-id="bdc35-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bdc35-132">System.String</span></span>

## <span data-ttu-id="bdc35-133">輸出</span><span class="sxs-lookup"><span data-stu-id="bdc35-133">OUTPUTS</span></span>

### <span data-ttu-id="bdc35-134">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="bdc35-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bdc35-135">筆記</span><span class="sxs-lookup"><span data-stu-id="bdc35-135">NOTES</span></span>

## <span data-ttu-id="bdc35-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdc35-136">RELATED LINKS</span></span>

[<span data-ttu-id="bdc35-137">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="bdc35-138">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="bdc35-139">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="bdc35-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="bdc35-141">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="bdc35-142">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="bdc35-143">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdc35-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


