---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 769fd151f68da6a38c1cf4d5b3636d7990a92943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447070"
---
# <span data-ttu-id="312fd-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="312fd-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="312fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="312fd-102">SYNOPSIS</span></span>
<span data-ttu-id="312fd-103">取得公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="312fd-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="312fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="312fd-104">SYNTAX</span></span>

### <span data-ttu-id="312fd-105">NoExpandStandAloneIp (預設) </span><span class="sxs-lookup"><span data-stu-id="312fd-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312fd-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="312fd-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312fd-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="312fd-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312fd-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="312fd-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="312fd-109">說明</span><span class="sxs-lookup"><span data-stu-id="312fd-109">DESCRIPTION</span></span>
<span data-ttu-id="312fd-110">**AzureRmPublicIPAddress** Cmdlet 會取得資源群組中的一個或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="312fd-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="312fd-111">示例</span><span class="sxs-lookup"><span data-stu-id="312fd-111">EXAMPLES</span></span>

### <span data-ttu-id="312fd-112">1：取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="312fd-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="312fd-113">這個命令會取得「資源群組」 $rgName 中名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="312fd-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="312fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="312fd-114">PARAMETERS</span></span>

### <span data-ttu-id="312fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312fd-115">-DefaultProfile</span></span>
<span data-ttu-id="312fd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="312fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="312fd-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="312fd-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="312fd-118">-IpConfigurationName</span></span>
<span data-ttu-id="312fd-119">網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="312fd-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="312fd-120">-Name</span></span>
<span data-ttu-id="312fd-121">指定此 Cmdlet 所取得之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="312fd-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="312fd-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="312fd-123">虛擬機器網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="312fd-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="312fd-125">指定包含此 Cmdlet 所取得之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="312fd-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="312fd-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="312fd-127">虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="312fd-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="312fd-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="312fd-129">虛擬機器的規模集名稱。</span><span class="sxs-lookup"><span data-stu-id="312fd-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312fd-130">CommonParameters</span></span>
<span data-ttu-id="312fd-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="312fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312fd-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="312fd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312fd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="312fd-133">INPUTS</span></span>

### <span data-ttu-id="312fd-134">所有</span><span class="sxs-lookup"><span data-stu-id="312fd-134">None</span></span>
<span data-ttu-id="312fd-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="312fd-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="312fd-136">輸出</span><span class="sxs-lookup"><span data-stu-id="312fd-136">OUTPUTS</span></span>

### <span data-ttu-id="312fd-137">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="312fd-137">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="312fd-138">筆記</span><span class="sxs-lookup"><span data-stu-id="312fd-138">NOTES</span></span>

## <span data-ttu-id="312fd-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="312fd-139">RELATED LINKS</span></span>

[<span data-ttu-id="312fd-140">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="312fd-140">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="312fd-141">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="312fd-141">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="312fd-142">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="312fd-142">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


