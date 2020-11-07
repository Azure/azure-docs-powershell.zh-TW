---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794405"
---
# <span data-ttu-id="e56ca-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e56ca-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="e56ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e56ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e56ca-103">取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="e56ca-103">Gets a network interface.</span></span>

## <span data-ttu-id="e56ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="e56ca-104">SYNTAX</span></span>

### <span data-ttu-id="e56ca-105">NoExpandStandAloneNic (預設) </span><span class="sxs-lookup"><span data-stu-id="e56ca-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56ca-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="e56ca-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56ca-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="e56ca-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56ca-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="e56ca-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e56ca-109">說明</span><span class="sxs-lookup"><span data-stu-id="e56ca-109">DESCRIPTION</span></span>
<span data-ttu-id="e56ca-110">**AzNetworkInterface** Cmdlet 會取得 azure 網路介面或資源群組中的 azure 網路介面清單。</span><span class="sxs-lookup"><span data-stu-id="e56ca-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="e56ca-111">示例</span><span class="sxs-lookup"><span data-stu-id="e56ca-111">EXAMPLES</span></span>

### <span data-ttu-id="e56ca-112">範例1：取得所有網路介面</span><span class="sxs-lookup"><span data-stu-id="e56ca-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="e56ca-113">這個命令會取得目前訂閱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="e56ca-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="e56ca-114">範例2：取得所有具有特定配定狀態的網路介面</span><span class="sxs-lookup"><span data-stu-id="e56ca-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="e56ca-115">這個命令會取得名為 ResourceGroup1 的資源群組中的所有網路介面，且該資源群組的 [已成功] 提供狀態。</span><span class="sxs-lookup"><span data-stu-id="e56ca-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="e56ca-116">參數</span><span class="sxs-lookup"><span data-stu-id="e56ca-116">PARAMETERS</span></span>

### <span data-ttu-id="e56ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56ca-117">-DefaultProfile</span></span>
<span data-ttu-id="e56ca-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e56ca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e56ca-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e56ca-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56ca-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e56ca-120">-Name</span></span>
<span data-ttu-id="e56ca-121">指定此 Cmdlet 所取得之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="e56ca-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e56ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="e56ca-123">指定此 Cmdlet 取得網路介面之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e56ca-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56ca-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="e56ca-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="e56ca-125">指定此 Cmdlet 取得網路介面之虛擬機器規模集的虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="e56ca-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56ca-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e56ca-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="e56ca-127">指定此 Cmdlet 取得網路介面的虛擬機器規模集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e56ca-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56ca-128">CommonParameters</span></span>
<span data-ttu-id="e56ca-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e56ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56ca-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e56ca-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56ca-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e56ca-131">INPUTS</span></span>

## <span data-ttu-id="e56ca-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e56ca-132">OUTPUTS</span></span>

### <span data-ttu-id="e56ca-133">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e56ca-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e56ca-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e56ca-134">NOTES</span></span>

## <span data-ttu-id="e56ca-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e56ca-135">RELATED LINKS</span></span>

[<span data-ttu-id="e56ca-136">新-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e56ca-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="e56ca-137">移除-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e56ca-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="e56ca-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e56ca-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


