---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454892"
---
# <span data-ttu-id="1f55d-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f55d-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="1f55d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f55d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f55d-103">取得公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1f55d-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f55d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f55d-104">SYNTAX</span></span>

### <span data-ttu-id="1f55d-105">NoExpandStandAloneIp (預設) </span><span class="sxs-lookup"><span data-stu-id="1f55d-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f55d-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="1f55d-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f55d-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1f55d-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f55d-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1f55d-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f55d-109">說明</span><span class="sxs-lookup"><span data-stu-id="1f55d-109">DESCRIPTION</span></span>
<span data-ttu-id="1f55d-110">**AzureRmPublicIPAddress** Cmdlet 會取得資源群組中的一個或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1f55d-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="1f55d-111">示例</span><span class="sxs-lookup"><span data-stu-id="1f55d-111">EXAMPLES</span></span>

### <span data-ttu-id="1f55d-112">1：取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="1f55d-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="1f55d-113">這個命令會取得「資源群組」 $rgName 中名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="1f55d-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="1f55d-114">參數</span><span class="sxs-lookup"><span data-stu-id="1f55d-114">PARAMETERS</span></span>

### <span data-ttu-id="1f55d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1f55d-115">-ExpandResource</span></span>
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

### <span data-ttu-id="1f55d-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1f55d-116">-IpConfigurationName</span></span>
<span data-ttu-id="1f55d-117">網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-117">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="1f55d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f55d-118">-Name</span></span>
<span data-ttu-id="1f55d-119">指定此 Cmdlet 所取得之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1f55d-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1f55d-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="1f55d-121">虛擬機器網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-121">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="1f55d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f55d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f55d-123">指定包含此 Cmdlet 所取得之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1f55d-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="1f55d-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="1f55d-125">虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="1f55d-125">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="1f55d-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1f55d-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="1f55d-127">虛擬機器的規模集名稱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-127">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="1f55d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f55d-128">-DefaultProfile</span></span>
<span data-ttu-id="1f55d-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f55d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f55d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f55d-130">CommonParameters</span></span>
<span data-ttu-id="1f55d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f55d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f55d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f55d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f55d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1f55d-133">INPUTS</span></span>

## <span data-ttu-id="1f55d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1f55d-134">OUTPUTS</span></span>

### <span data-ttu-id="1f55d-135">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f55d-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1f55d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1f55d-136">NOTES</span></span>

## <span data-ttu-id="1f55d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f55d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f55d-138">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f55d-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1f55d-139">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f55d-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1f55d-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f55d-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


