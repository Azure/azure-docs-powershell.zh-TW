---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791950"
---
# <span data-ttu-id="6c901-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="6c901-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="6c901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c901-102">SYNOPSIS</span></span>
<span data-ttu-id="6c901-103">從資源群組更新私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6c901-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="6c901-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c901-104">SYNTAX</span></span>

### <span data-ttu-id="6c901-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="6c901-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c901-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c901-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c901-107">面向</span><span class="sxs-lookup"><span data-stu-id="6c901-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c901-108">說明</span><span class="sxs-lookup"><span data-stu-id="6c901-108">DESCRIPTION</span></span>
<span data-ttu-id="6c901-109">AzPrivateDnsZone Cmdlet 會從指定 **的** 資源群組中永久更新私人網功能變數名稱稱系統 (DNS) 區域。</span><span class="sxs-lookup"><span data-stu-id="6c901-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="6c901-110">您可以使用 *PrivateZone* 參數或使用管線運算子來傳遞 **PrivateDnsZone** 物件，或者也可以指定 *Name* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6c901-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6c901-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c901-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6c901-112">使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **PrivateDnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會更新，因為只有在已 (檢索到 DNS 區域資源的操作中，該區域就不會) 。</span><span class="sxs-lookup"><span data-stu-id="6c901-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="6c901-113">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6c901-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="6c901-114">這可以使用 *Overwrite* 參數加以取消，不論併發變更的情況為何都會更新該區域。</span><span class="sxs-lookup"><span data-stu-id="6c901-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="6c901-115">示例</span><span class="sxs-lookup"><span data-stu-id="6c901-115">EXAMPLES</span></span>

### <span data-ttu-id="6c901-116">範例1：更新私人區域</span><span class="sxs-lookup"><span data-stu-id="6c901-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="6c901-117">參數</span><span class="sxs-lookup"><span data-stu-id="6c901-117">PARAMETERS</span></span>

### <span data-ttu-id="6c901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c901-118">-DefaultProfile</span></span>
<span data-ttu-id="6c901-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6c901-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c901-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c901-120">-Name</span></span>
<span data-ttu-id="6c901-121">指定此 Cmdlet 更新之專用 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c901-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="6c901-122">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6c901-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="6c901-123">或者，您也可以使用 *zone* 參數指定私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6c901-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="6c901-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6c901-124">-Overwrite</span></span>
<span data-ttu-id="6c901-125">使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會更新，因為只有在已 (檢索到 DNS 區域資源的操作中，該區域就不會) 。</span><span class="sxs-lookup"><span data-stu-id="6c901-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="6c901-126">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6c901-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="6c901-127">這可以使用 *Overwrite* 參數加以取消，不論併發變更的情況為何都會更新該區域。</span><span class="sxs-lookup"><span data-stu-id="6c901-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6c901-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="6c901-128">-PrivateZone</span></span>
<span data-ttu-id="6c901-129">要設定的區域物件。</span><span class="sxs-lookup"><span data-stu-id="6c901-129">The zone object to set.</span></span>

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

### <span data-ttu-id="6c901-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c901-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c901-131">指定包含要更新之區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c901-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="6c901-132">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6c901-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="6c901-133">或者，您也可以使用 **DnsZone** 物件來指定私人 DNS 區域，方法是透過管線或 *zone* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="6c901-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="6c901-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c901-134">-ResourceId</span></span>
<span data-ttu-id="6c901-135">私人 DNS 區域 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="6c901-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="6c901-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c901-136">-Tag</span></span>
<span data-ttu-id="6c901-137">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6c901-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6c901-138">-確認</span><span class="sxs-lookup"><span data-stu-id="6c901-138">-Confirm</span></span>
<span data-ttu-id="6c901-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c901-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c901-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c901-140">-WhatIf</span></span>
<span data-ttu-id="6c901-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c901-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c901-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c901-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c901-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c901-143">CommonParameters</span></span>
<span data-ttu-id="6c901-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c901-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c901-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c901-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c901-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6c901-146">INPUTS</span></span>

### <span data-ttu-id="6c901-147">System.object</span><span class="sxs-lookup"><span data-stu-id="6c901-147">System.String</span></span>

### <span data-ttu-id="6c901-148">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="6c901-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="6c901-149">輸出</span><span class="sxs-lookup"><span data-stu-id="6c901-149">OUTPUTS</span></span>

### <span data-ttu-id="6c901-150">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="6c901-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="6c901-151">筆記</span><span class="sxs-lookup"><span data-stu-id="6c901-151">NOTES</span></span>

## <span data-ttu-id="6c901-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c901-152">RELATED LINKS</span></span>

[<span data-ttu-id="6c901-153">AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="6c901-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="6c901-154">新-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="6c901-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="6c901-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="6c901-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
