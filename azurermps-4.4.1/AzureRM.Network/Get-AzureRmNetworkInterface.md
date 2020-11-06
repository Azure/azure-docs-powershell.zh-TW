---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 42d5ef31b49f8abe5c8e582e0a85e8766a71b9a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455716"
---
# <span data-ttu-id="aeb3f-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aeb3f-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="aeb3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aeb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb3f-103">取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="aeb3f-104">SYNTAX</span></span>

### <span data-ttu-id="aeb3f-105">NoExpandStandAloneNic (預設) </span><span class="sxs-lookup"><span data-stu-id="aeb3f-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeb3f-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="aeb3f-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeb3f-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="aeb3f-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeb3f-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="aeb3f-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeb3f-109">說明</span><span class="sxs-lookup"><span data-stu-id="aeb3f-109">DESCRIPTION</span></span>
<span data-ttu-id="aeb3f-110">**AzureRmNetworkInterface** Cmdlet 會取得 azure 網路介面或資源群組中的 azure 網路介面清單。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="aeb3f-111">示例</span><span class="sxs-lookup"><span data-stu-id="aeb3f-111">EXAMPLES</span></span>

### <span data-ttu-id="aeb3f-112">範例1：取得所有網路介面</span><span class="sxs-lookup"><span data-stu-id="aeb3f-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="aeb3f-113">這個命令會取得目前訂閱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="aeb3f-114">範例2：取得所有具有特定配定狀態的網路介面</span><span class="sxs-lookup"><span data-stu-id="aeb3f-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="aeb3f-115">這個命令會取得名為 ResourceGroup1 的資源群組中的所有網路介面，且該資源群組的 [已成功] 提供狀態。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="aeb3f-116">參數</span><span class="sxs-lookup"><span data-stu-id="aeb3f-116">PARAMETERS</span></span>

### <span data-ttu-id="aeb3f-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="aeb3f-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb3f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="aeb3f-118">-Name</span></span>
<span data-ttu-id="aeb3f-119">指定此 Cmdlet 所取得之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-119">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb3f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb3f-120">-ResourceGroupName</span></span>
<span data-ttu-id="aeb3f-121">指定此 Cmdlet 取得網路介面之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-121">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb3f-122">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="aeb3f-122">-VirtualMachineIndex</span></span>
<span data-ttu-id="aeb3f-123">指定此 Cmdlet 取得網路介面之虛擬機器規模集的虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-123">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb3f-124">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aeb3f-124">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="aeb3f-125">指定此 Cmdlet 取得網路介面的虛擬機器規模集的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-125">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb3f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb3f-126">-DefaultProfile</span></span>
<span data-ttu-id="aeb3f-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb3f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb3f-128">CommonParameters</span></span>
<span data-ttu-id="aeb3f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb3f-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aeb3f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb3f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="aeb3f-131">INPUTS</span></span>

## <span data-ttu-id="aeb3f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="aeb3f-132">OUTPUTS</span></span>

### <span data-ttu-id="aeb3f-133">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aeb3f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="aeb3f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="aeb3f-134">NOTES</span></span>

## <span data-ttu-id="aeb3f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="aeb3f-135">RELATED LINKS</span></span>

[<span data-ttu-id="aeb3f-136">新-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aeb3f-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="aeb3f-137">移除-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aeb3f-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="aeb3f-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aeb3f-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


