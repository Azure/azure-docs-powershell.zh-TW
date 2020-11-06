---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448387"
---
# <span data-ttu-id="33c55-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c55-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="33c55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33c55-102">SYNOPSIS</span></span>
<span data-ttu-id="33c55-103">取得公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="33c55-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c55-104">句法</span><span class="sxs-lookup"><span data-stu-id="33c55-104">SYNTAX</span></span>

### <span data-ttu-id="33c55-105">NoExpandStandAloneIp (預設) </span><span class="sxs-lookup"><span data-stu-id="33c55-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c55-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="33c55-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c55-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="33c55-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c55-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="33c55-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33c55-109">說明</span><span class="sxs-lookup"><span data-stu-id="33c55-109">DESCRIPTION</span></span>
<span data-ttu-id="33c55-110">**AzureRmPublicIPAddress** Cmdlet 會取得資源群組中的一個或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="33c55-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="33c55-111">示例</span><span class="sxs-lookup"><span data-stu-id="33c55-111">EXAMPLES</span></span>

### <span data-ttu-id="33c55-112">1：取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="33c55-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="33c55-113">這個命令會取得「資源群組」 $rgName 中名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="33c55-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="33c55-114">參數</span><span class="sxs-lookup"><span data-stu-id="33c55-114">PARAMETERS</span></span>

### <span data-ttu-id="33c55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c55-115">-DefaultProfile</span></span>
<span data-ttu-id="33c55-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33c55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33c55-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="33c55-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="33c55-118">-IpConfigurationName</span></span>
<span data-ttu-id="33c55-119">網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="33c55-119">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="33c55-120">-Name</span></span>
<span data-ttu-id="33c55-121">指定此 Cmdlet 所取得之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="33c55-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="33c55-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="33c55-123">虛擬機器網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="33c55-123">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c55-124">-ResourceGroupName</span></span>
<span data-ttu-id="33c55-125">指定包含此 Cmdlet 所取得之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33c55-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="33c55-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="33c55-127">虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="33c55-127">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33c55-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="33c55-129">虛擬機器的規模集名稱。</span><span class="sxs-lookup"><span data-stu-id="33c55-129">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c55-130">CommonParameters</span></span>
<span data-ttu-id="33c55-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33c55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c55-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33c55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c55-133">輸入</span><span class="sxs-lookup"><span data-stu-id="33c55-133">INPUTS</span></span>

### <span data-ttu-id="33c55-134">System.object</span><span class="sxs-lookup"><span data-stu-id="33c55-134">System.String</span></span>

## <span data-ttu-id="33c55-135">輸出</span><span class="sxs-lookup"><span data-stu-id="33c55-135">OUTPUTS</span></span>

### <span data-ttu-id="33c55-136">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="33c55-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="33c55-137">筆記</span><span class="sxs-lookup"><span data-stu-id="33c55-137">NOTES</span></span>

## <span data-ttu-id="33c55-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="33c55-138">RELATED LINKS</span></span>

[<span data-ttu-id="33c55-139">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c55-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="33c55-140">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c55-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="33c55-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c55-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


