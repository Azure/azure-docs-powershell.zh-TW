---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139355"
---
# <span data-ttu-id="e7f7e-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="e7f7e-101">Get-AzHost</span></span>

## <span data-ttu-id="e7f7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f7e-103">取得或列出主機。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-103">Get or list hosts.</span></span>

## <span data-ttu-id="e7f7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7f7e-104">SYNTAX</span></span>

### <span data-ttu-id="e7f7e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="e7f7e-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f7e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e7f7e-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f7e-107">說明</span><span class="sxs-lookup"><span data-stu-id="e7f7e-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f7e-108">這個 Cmdlet 會取得主機群組中的主機。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="e7f7e-109">如果沒有指定主機名稱，這個 Cmdlet 也會列出主機群組中的所有主機。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="e7f7e-110">示例</span><span class="sxs-lookup"><span data-stu-id="e7f7e-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f7e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e7f7e-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="e7f7e-112">這個命令會傳回主機。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-112">This command returns a host.</span></span>

### <span data-ttu-id="e7f7e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e7f7e-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="e7f7e-114">這個命令會傳回主機的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="e7f7e-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e7f7e-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="e7f7e-116">這個命令會傳回指定主機群組中的所有主機。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="e7f7e-117">參數</span><span class="sxs-lookup"><span data-stu-id="e7f7e-117">PARAMETERS</span></span>

### <span data-ttu-id="e7f7e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f7e-118">-DefaultProfile</span></span>
<span data-ttu-id="e7f7e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f7e-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f7e-120">-HostGroupName</span></span>
<span data-ttu-id="e7f7e-121">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f7e-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="e7f7e-122">-InstanceView</span></span>
<span data-ttu-id="e7f7e-123">表示此 Cmdlet 只會取得主機的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f7e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7f7e-124">-Name</span></span>
<span data-ttu-id="e7f7e-125">主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7f7e-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e7f7e-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f7e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f7e-128">-ResourceId</span></span>
<span data-ttu-id="e7f7e-129">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f7e-130">CommonParameters</span></span>
<span data-ttu-id="e7f7e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f7e-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f7e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e7f7e-133">INPUTS</span></span>

### <span data-ttu-id="e7f7e-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e7f7e-134">System.String</span></span>

## <span data-ttu-id="e7f7e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e7f7e-135">OUTPUTS</span></span>

### <span data-ttu-id="e7f7e-136">PSHost 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e7f7e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="e7f7e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e7f7e-137">NOTES</span></span>

## <span data-ttu-id="e7f7e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7f7e-138">RELATED LINKS</span></span>
