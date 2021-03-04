---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: b28153176fdc591bc7298b45f75e8befa59e8554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910949"
---
# <span data-ttu-id="746d3-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="746d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="746d3-102">SYNOPSIS</span></span>
<span data-ttu-id="746d3-103">更新資源群組中的私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="746d3-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="746d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="746d3-104">SYNTAX</span></span>

### <span data-ttu-id="746d3-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="746d3-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="746d3-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746d3-107">物件</span><span class="sxs-lookup"><span data-stu-id="746d3-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746d3-108">描述</span><span class="sxs-lookup"><span data-stu-id="746d3-108">DESCRIPTION</span></span>
<span data-ttu-id="746d3-109">**Set-AzPrivateDnsZone Cmdlet** 會從指定的資源群組 (DNS) 區域永久更新私人網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="746d3-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="746d3-110">您可以使用 PrivateZone 參數或管道運算子傳遞 **PrivateDnsZone** 物件，或者您也可以指定 *Name* 和 *ResourceGroupName* 參數。 </span><span class="sxs-lookup"><span data-stu-id="746d3-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="746d3-111">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="746d3-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="746d3-112">使用透過管線或區域參數 (傳遞的 **PrivateDnsZone** 物件) 來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會更新，因為已取回本地 **PrivateDnsZone** 物件 (只有在 DNS 區域資源計數為變更時執行作業，區域中的記錄集作業不會更新) 。</span><span class="sxs-lookup"><span data-stu-id="746d3-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="746d3-113">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="746d3-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="746d3-114">您可以使用覆寫參數隱藏此設定，無論同時變更，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="746d3-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="746d3-115">例子</span><span class="sxs-lookup"><span data-stu-id="746d3-115">EXAMPLES</span></span>

### <span data-ttu-id="746d3-116">範例 1：更新私人區域</span><span class="sxs-lookup"><span data-stu-id="746d3-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="746d3-117">參數</span><span class="sxs-lookup"><span data-stu-id="746d3-117">PARAMETERS</span></span>

### <span data-ttu-id="746d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746d3-118">-DefaultProfile</span></span>
<span data-ttu-id="746d3-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="746d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="746d3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="746d3-120">-Name</span></span>
<span data-ttu-id="746d3-121">指定此 Cmdlet 更新的專用 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="746d3-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="746d3-122">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="746d3-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="746d3-123">或者，您可以使用 Zone 參數指定私人 DNS *區域。*</span><span class="sxs-lookup"><span data-stu-id="746d3-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-124">-覆寫</span><span class="sxs-lookup"><span data-stu-id="746d3-124">-Overwrite</span></span>
<span data-ttu-id="746d3-125">使用透過管線或區域參數) 傳遞 **的 PrivateDnsZone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會更新，因為已取回本地 **Dns Zone** 物件 (只有直接在 DNS 區域資源計數上執行作業做為變更，區域中的記錄集作業不會) 。</span><span class="sxs-lookup"><span data-stu-id="746d3-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="746d3-126">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="746d3-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="746d3-127">您可以使用覆寫參數隱藏此設定，無論同時變更，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="746d3-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="746d3-128">-PrivateZone</span></span>
<span data-ttu-id="746d3-129">要設定的區域物件。</span><span class="sxs-lookup"><span data-stu-id="746d3-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="746d3-131">指定包含要更新之區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="746d3-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="746d3-132">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="746d3-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="746d3-133">或者，您可以使用透過管線或 Zone 參數傳遞 **的 Dns Zone** 物件來指定私人 *DNS* 區域。</span><span class="sxs-lookup"><span data-stu-id="746d3-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="746d3-134">-ResourceId</span></span>
<span data-ttu-id="746d3-135">私人 DNS 區域資源ID。</span><span class="sxs-lookup"><span data-stu-id="746d3-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-136">-標記</span><span class="sxs-lookup"><span data-stu-id="746d3-136">-Tag</span></span>
<span data-ttu-id="746d3-137">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="746d3-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-138">-確認</span><span class="sxs-lookup"><span data-stu-id="746d3-138">-Confirm</span></span>
<span data-ttu-id="746d3-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="746d3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746d3-140">-WhatIf</span></span>
<span data-ttu-id="746d3-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="746d3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746d3-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="746d3-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746d3-143">CommonParameters</span></span>
<span data-ttu-id="746d3-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="746d3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746d3-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="746d3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746d3-146">輸入</span><span class="sxs-lookup"><span data-stu-id="746d3-146">INPUTS</span></span>

### <span data-ttu-id="746d3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="746d3-147">System.String</span></span>

### <span data-ttu-id="746d3-148">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="746d3-149">輸出</span><span class="sxs-lookup"><span data-stu-id="746d3-149">OUTPUTS</span></span>

### <span data-ttu-id="746d3-150">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="746d3-151">筆記</span><span class="sxs-lookup"><span data-stu-id="746d3-151">NOTES</span></span>

## <span data-ttu-id="746d3-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="746d3-152">RELATED LINKS</span></span>

[<span data-ttu-id="746d3-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="746d3-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="746d3-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="746d3-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
