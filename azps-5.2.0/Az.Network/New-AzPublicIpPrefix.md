---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275440"
---
# <span data-ttu-id="37d4c-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="37d4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="37d4c-103">建立公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="37d4c-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="37d4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="37d4c-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="37d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="37d4c-106">**新的-AzPublicIpPrefix** Cmdlet 會建立公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="37d4c-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="37d4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="37d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="37d4c-108">範例1：建立新的公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="37d4c-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="37d4c-109">這個命令會建立新的公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="37d4c-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="37d4c-110">範例2：建立新的全域公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="37d4c-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="37d4c-111">這個命令會建立新的全域公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="37d4c-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="37d4c-112">參數</span><span class="sxs-lookup"><span data-stu-id="37d4c-112">PARAMETERS</span></span>

### <span data-ttu-id="37d4c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37d4c-113">-AsJob</span></span>
<span data-ttu-id="37d4c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37d4c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37d4c-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-115">-CustomIpPrefix</span></span>
<span data-ttu-id="37d4c-116">此 PublicIpPrefix 將與之關聯的 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d4c-117">-DefaultProfile</span></span>
<span data-ttu-id="37d4c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37d4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d4c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="37d4c-119">-Force</span></span>
<span data-ttu-id="37d4c-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="37d4c-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="37d4c-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="37d4c-121">-IpAddressVersion</span></span>
<span data-ttu-id="37d4c-122">公用 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="37d4c-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="37d4c-123">-IpTag</span></span>
<span data-ttu-id="37d4c-124">IpTag 清單]。</span><span class="sxs-lookup"><span data-stu-id="37d4c-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-125">-位置</span><span class="sxs-lookup"><span data-stu-id="37d4c-125">-Location</span></span>
<span data-ttu-id="37d4c-126">公用 IP 首碼位置。</span><span class="sxs-lookup"><span data-stu-id="37d4c-126">The public IP prefix location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="37d4c-127">-Name</span></span>
<span data-ttu-id="37d4c-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="37d4c-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="37d4c-129">-PrefixLength</span></span>
<span data-ttu-id="37d4c-130">PublicIPPrefix 長度</span><span class="sxs-lookup"><span data-stu-id="37d4c-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d4c-131">-ResourceGroupName</span></span>
<span data-ttu-id="37d4c-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37d4c-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="37d4c-133">-Sku</span></span>
<span data-ttu-id="37d4c-134">公用 IP 首碼 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="37d4c-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="37d4c-135">-Tag</span></span>
<span data-ttu-id="37d4c-136">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="37d4c-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-137">層級</span><span class="sxs-lookup"><span data-stu-id="37d4c-137">-Tier</span></span>
<span data-ttu-id="37d4c-138">公用 IP 首碼 Sku 層。</span><span class="sxs-lookup"><span data-stu-id="37d4c-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="37d4c-139">-Zone</span></span>
<span data-ttu-id="37d4c-140">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="37d4c-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="37d4c-141">-Confirm</span></span>
<span data-ttu-id="37d4c-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37d4c-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d4c-143">-WhatIf</span></span>
<span data-ttu-id="37d4c-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37d4c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d4c-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37d4c-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d4c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d4c-146">CommonParameters</span></span>
<span data-ttu-id="37d4c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37d4c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d4c-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37d4c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d4c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="37d4c-149">INPUTS</span></span>

### <span data-ttu-id="37d4c-150">System.object</span><span class="sxs-lookup"><span data-stu-id="37d4c-150">System.String</span></span>

### <span data-ttu-id="37d4c-151">System.object</span><span class="sxs-lookup"><span data-stu-id="37d4c-151">System.UInt16</span></span>

### <span data-ttu-id="37d4c-152">PSPublicIpPrefixTag [] （[]）</span><span class="sxs-lookup"><span data-stu-id="37d4c-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="37d4c-153">System.object []</span><span class="sxs-lookup"><span data-stu-id="37d4c-153">System.String[]</span></span>

### <span data-ttu-id="37d4c-154">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="37d4c-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="37d4c-155">輸出</span><span class="sxs-lookup"><span data-stu-id="37d4c-155">OUTPUTS</span></span>

### <span data-ttu-id="37d4c-156">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="37d4c-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="37d4c-157">筆記</span><span class="sxs-lookup"><span data-stu-id="37d4c-157">NOTES</span></span>

## <span data-ttu-id="37d4c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="37d4c-158">RELATED LINKS</span></span>

[<span data-ttu-id="37d4c-159">AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="37d4c-160">移除-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="37d4c-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="37d4c-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
