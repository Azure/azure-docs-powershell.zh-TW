---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: d54b2952c617782ec30193372b430785c0a8b79d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905317"
---
# <span data-ttu-id="594e5-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="594e5-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="594e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="594e5-102">SYNOPSIS</span></span>
<span data-ttu-id="594e5-103">從私人 DNS 區域刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="594e5-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="594e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="594e5-104">SYNTAX</span></span>

### <span data-ttu-id="594e5-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="594e5-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="594e5-106">混合</span><span class="sxs-lookup"><span data-stu-id="594e5-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594e5-107">物件</span><span class="sxs-lookup"><span data-stu-id="594e5-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594e5-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="594e5-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594e5-109">描述</span><span class="sxs-lookup"><span data-stu-id="594e5-109">DESCRIPTION</span></span>
<span data-ttu-id="594e5-110">此Remove-AzPrivateDnsRecordSet Cmdlet 會從指定的區域刪除指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="594e5-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="594e5-111">您無法刪除在私人區域頂點自動建立之 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="594e5-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="594e5-112">您可以使用管線運算子或參數或 ResourceId，將 RecordSet 物件傳遞到此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="594e5-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="594e5-113">若要在不使用 RecordSet 物件的情況下，根據名稱和類型識別記錄，您必須使用管線運算子或參數，將區域以 PSPrivateDnsZone 物件傳遞至此 Cmdlet，或者您也可以指定 ZoneName 和 ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="594e5-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="594e5-114">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="594e5-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="594e5-115">使用 RecordSet 物件指定記錄集時，如果自本地 RecordSet 物件被取回後，已在 Azure Private DNS 中變更記錄集，則記錄集不會刪除。</span><span class="sxs-lookup"><span data-stu-id="594e5-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="594e5-116">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="594e5-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="594e5-117">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="594e5-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="594e5-118">例子</span><span class="sxs-lookup"><span data-stu-id="594e5-118">EXAMPLES</span></span>

### <span data-ttu-id="594e5-119">範例 1：移除記錄集</span><span class="sxs-lookup"><span data-stu-id="594e5-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="594e5-120">第一個命令會獲得指定的記錄集，然後將它儲存在$RecordSet變數中。第二個命令會移除 $RecordSet。</span><span class="sxs-lookup"><span data-stu-id="594e5-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="594e5-121">範例 2：移除記錄集並隱藏所有確認</span><span class="sxs-lookup"><span data-stu-id="594e5-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="594e5-122">第一個命令會獲得指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="594e5-122">The first command gets the specified record set.</span></span> <span data-ttu-id="594e5-123">第二個命令會刪除記錄集，即使同時已變更。</span><span class="sxs-lookup"><span data-stu-id="594e5-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="594e5-124">確認提示會隱藏。</span><span class="sxs-lookup"><span data-stu-id="594e5-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="594e5-125">參數</span><span class="sxs-lookup"><span data-stu-id="594e5-125">PARAMETERS</span></span>

### <span data-ttu-id="594e5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594e5-126">-DefaultProfile</span></span>
<span data-ttu-id="594e5-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="594e5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594e5-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="594e5-128">-Name</span></span>
<span data-ttu-id="594e5-129">記錄集的記錄名稱會 (區功能變數名稱稱，且不會以終止點) 。</span><span class="sxs-lookup"><span data-stu-id="594e5-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-130">-覆寫</span><span class="sxs-lookup"><span data-stu-id="594e5-130">-Overwrite</span></span>
<span data-ttu-id="594e5-131">請勿使用 RecordSet 參數的 ETag 欄位進行開放式並行檢查。</span><span class="sxs-lookup"><span data-stu-id="594e5-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="594e5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="594e5-132">-PassThru</span></span>
<span data-ttu-id="594e5-133">用來傳遞作業中 (布林值) 刪除管線下一個私人區域。</span><span class="sxs-lookup"><span data-stu-id="594e5-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="594e5-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="594e5-134">-RecordSet</span></span>
<span data-ttu-id="594e5-135">要新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="594e5-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="594e5-136">-RecordType</span></span>
<span data-ttu-id="594e5-137">記錄集的私人 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="594e5-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594e5-138">-ResourceGroupName</span></span>
<span data-ttu-id="594e5-139">區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="594e5-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="594e5-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="594e5-140">-ResourceId</span></span>
<span data-ttu-id="594e5-141">私人 DNS RecordSet ResourceID。</span><span class="sxs-lookup"><span data-stu-id="594e5-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="594e5-142">-區域</span><span class="sxs-lookup"><span data-stu-id="594e5-142">-Zone</span></span>
<span data-ttu-id="594e5-143">PrivateDnsZone 物件代表要建立記錄集的區域。</span><span class="sxs-lookup"><span data-stu-id="594e5-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="594e5-144">-ZoneName</span></span>
<span data-ttu-id="594e5-145">記錄集存在的區域 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="594e5-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="594e5-146">-確認</span><span class="sxs-lookup"><span data-stu-id="594e5-146">-Confirm</span></span>
<span data-ttu-id="594e5-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="594e5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594e5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594e5-148">-WhatIf</span></span>
<span data-ttu-id="594e5-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="594e5-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594e5-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="594e5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594e5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594e5-151">CommonParameters</span></span>
<span data-ttu-id="594e5-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="594e5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594e5-153">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="594e5-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594e5-154">輸入</span><span class="sxs-lookup"><span data-stu-id="594e5-154">INPUTS</span></span>

### <span data-ttu-id="594e5-155">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="594e5-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="594e5-156">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="594e5-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="594e5-157">System.String</span><span class="sxs-lookup"><span data-stu-id="594e5-157">System.String</span></span>

## <span data-ttu-id="594e5-158">輸出</span><span class="sxs-lookup"><span data-stu-id="594e5-158">OUTPUTS</span></span>

### <span data-ttu-id="594e5-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="594e5-159">System.Boolean</span></span>

## <span data-ttu-id="594e5-160">筆記</span><span class="sxs-lookup"><span data-stu-id="594e5-160">NOTES</span></span>

## <span data-ttu-id="594e5-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="594e5-161">RELATED LINKS</span></span>
