---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626059"
---
# <span data-ttu-id="9e95a-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e95a-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="9e95a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e95a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e95a-103">建立公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="9e95a-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e95a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e95a-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e95a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e95a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e95a-106">**新的-AzureRmPublicIpPrefix** Cmdlet 會建立公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="9e95a-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="9e95a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e95a-107">EXAMPLES</span></span>

### <span data-ttu-id="9e95a-108">1：建立新的公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="9e95a-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="9e95a-109">這個命令會建立新的公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="9e95a-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="9e95a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e95a-110">PARAMETERS</span></span>

### <span data-ttu-id="9e95a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e95a-111">-AsJob</span></span>
<span data-ttu-id="9e95a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e95a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e95a-113">-DefaultProfile</span></span>
<span data-ttu-id="9e95a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e95a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e95a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9e95a-115">-Force</span></span>
<span data-ttu-id="9e95a-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="9e95a-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9e95a-117">-IpAddressVersion</span></span>
<span data-ttu-id="9e95a-118">公用 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="9e95a-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="9e95a-119">-IpTag</span></span>
<span data-ttu-id="9e95a-120">IpTag 清單]。</span><span class="sxs-lookup"><span data-stu-id="9e95a-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9e95a-121">-Location</span></span>
<span data-ttu-id="9e95a-122">公用 IP 首碼位置。</span><span class="sxs-lookup"><span data-stu-id="9e95a-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e95a-123">-Name</span></span>
<span data-ttu-id="9e95a-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9e95a-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="9e95a-125">-PrefixLength</span></span>
<span data-ttu-id="9e95a-126">PublicIPPrefix 長度</span><span class="sxs-lookup"><span data-stu-id="9e95a-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e95a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e95a-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e95a-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="9e95a-129">-Sku</span></span>
<span data-ttu-id="9e95a-130">公用 IP 首碼 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="9e95a-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e95a-131">-Tag</span></span>
<span data-ttu-id="9e95a-132">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="9e95a-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e95a-133">-Zone</span></span>
<span data-ttu-id="9e95a-134">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="9e95a-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="9e95a-135">-Confirm</span></span>
<span data-ttu-id="9e95a-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e95a-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e95a-137">-WhatIf</span></span>
<span data-ttu-id="9e95a-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e95a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e95a-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e95a-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e95a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e95a-140">CommonParameters</span></span>
<span data-ttu-id="9e95a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e95a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e95a-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e95a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e95a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9e95a-143">INPUTS</span></span>

### <span data-ttu-id="9e95a-144">System.object</span><span class="sxs-lookup"><span data-stu-id="9e95a-144">System.String</span></span>
<span data-ttu-id="9e95a-145">System.object. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]] System. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e95a-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="9e95a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9e95a-146">OUTPUTS</span></span>

### <span data-ttu-id="9e95a-147">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e95a-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="9e95a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9e95a-148">NOTES</span></span>

## <span data-ttu-id="9e95a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e95a-149">RELATED LINKS</span></span>
