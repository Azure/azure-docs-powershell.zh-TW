---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794368"
---
# <span data-ttu-id="1b113-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b113-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="1b113-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b113-102">SYNOPSIS</span></span>
<span data-ttu-id="1b113-103">取得公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b113-103">Gets a public IP address.</span></span>

## <span data-ttu-id="1b113-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b113-104">SYNTAX</span></span>

### <span data-ttu-id="1b113-105">NoExpandStandAloneIp (預設) </span><span class="sxs-lookup"><span data-stu-id="1b113-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b113-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="1b113-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b113-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1b113-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b113-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="1b113-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b113-109">說明</span><span class="sxs-lookup"><span data-stu-id="1b113-109">DESCRIPTION</span></span>
<span data-ttu-id="1b113-110">**AzPublicIPAddress** Cmdlet 會取得資源群組中的一個或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b113-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="1b113-111">示例</span><span class="sxs-lookup"><span data-stu-id="1b113-111">EXAMPLES</span></span>

### <span data-ttu-id="1b113-112">1：取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="1b113-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="1b113-113">這個命令會取得「資源群組」 $rgName 中名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="1b113-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="1b113-114">參數</span><span class="sxs-lookup"><span data-stu-id="1b113-114">PARAMETERS</span></span>

### <span data-ttu-id="1b113-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b113-115">-DefaultProfile</span></span>
<span data-ttu-id="1b113-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b113-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b113-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1b113-117">-ExpandResource</span></span>
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

### <span data-ttu-id="1b113-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1b113-118">-IpConfigurationName</span></span>
<span data-ttu-id="1b113-119">網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1b113-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="1b113-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b113-120">-Name</span></span>
<span data-ttu-id="1b113-121">指定此 Cmdlet 所取得之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b113-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1b113-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1b113-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="1b113-123">虛擬機器網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="1b113-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="1b113-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b113-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b113-125">指定包含此 Cmdlet 所取得之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b113-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1b113-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="1b113-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="1b113-127">虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="1b113-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="1b113-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1b113-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="1b113-129">虛擬機器的規模集名稱。</span><span class="sxs-lookup"><span data-stu-id="1b113-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="1b113-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b113-130">CommonParameters</span></span>
<span data-ttu-id="1b113-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b113-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b113-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b113-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b113-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1b113-133">INPUTS</span></span>

## <span data-ttu-id="1b113-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1b113-134">OUTPUTS</span></span>

### <span data-ttu-id="1b113-135">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b113-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1b113-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1b113-136">NOTES</span></span>

## <span data-ttu-id="1b113-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b113-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b113-138">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b113-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="1b113-139">移除-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b113-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="1b113-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b113-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


