---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905401"
---
# <span data-ttu-id="8229c-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="8229c-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="8229c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8229c-102">SYNOPSIS</span></span>
<span data-ttu-id="8229c-103">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="8229c-103">Create a PSBackend object</span></span>

## <span data-ttu-id="8229c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8229c-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8229c-105">描述</span><span class="sxs-lookup"><span data-stu-id="8229c-105">DESCRIPTION</span></span>
<span data-ttu-id="8229c-106">建立 PSBackend 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="8229c-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="8229c-107">例子</span><span class="sxs-lookup"><span data-stu-id="8229c-107">EXAMPLES</span></span>

### <span data-ttu-id="8229c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8229c-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="8229c-109">建立 PSBackend 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="8229c-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="8229c-110">參數</span><span class="sxs-lookup"><span data-stu-id="8229c-110">PARAMETERS</span></span>

### <span data-ttu-id="8229c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="8229c-111">-Address</span></span>
<span data-ttu-id="8229c-112">後端位置 (IP 位址或 FQDN) </span><span class="sxs-lookup"><span data-stu-id="8229c-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-113">-後端HostHeader</span><span class="sxs-lookup"><span data-stu-id="8229c-113">-BackendHostHeader</span></span>
<span data-ttu-id="8229c-114">要當做主機標題的值，會送到後端。</span><span class="sxs-lookup"><span data-stu-id="8229c-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="8229c-115">預設值是後端位址。</span><span class="sxs-lookup"><span data-stu-id="8229c-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8229c-116">-DefaultProfile</span></span>
<span data-ttu-id="8229c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8229c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8229c-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8229c-118">-EnabledState</span></span>
<span data-ttu-id="8229c-119">是否要啟用使用此後端。</span><span class="sxs-lookup"><span data-stu-id="8229c-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="8229c-120">預設值為啟用</span><span class="sxs-lookup"><span data-stu-id="8229c-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-121">-HTTPPort</span><span class="sxs-lookup"><span data-stu-id="8229c-121">-HttpPort</span></span>
<span data-ttu-id="8229c-122">HTTP TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="8229c-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="8229c-123">必須介於 1 到 65535 之間。</span><span class="sxs-lookup"><span data-stu-id="8229c-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="8229c-124">預設值為 80。</span><span class="sxs-lookup"><span data-stu-id="8229c-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-125">-HTTPsPort</span><span class="sxs-lookup"><span data-stu-id="8229c-125">-HttpsPort</span></span>
<span data-ttu-id="8229c-126">HTTPS TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="8229c-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="8229c-127">必須介於 1 到 65535 之間。</span><span class="sxs-lookup"><span data-stu-id="8229c-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="8229c-128">預設值為 443</span><span class="sxs-lookup"><span data-stu-id="8229c-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="8229c-129">-Priority</span></span>
<span data-ttu-id="8229c-130">負載平衡的優先順序。</span><span class="sxs-lookup"><span data-stu-id="8229c-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="8229c-131">必須介於 1 到 5 之間。</span><span class="sxs-lookup"><span data-stu-id="8229c-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="8229c-132">預設值為 1</span><span class="sxs-lookup"><span data-stu-id="8229c-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="8229c-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="8229c-134">私人連結資源的別名。</span><span class="sxs-lookup"><span data-stu-id="8229c-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="8229c-135">填上此選擇性欄位表示此後端為'私人'</span><span class="sxs-lookup"><span data-stu-id="8229c-135">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="8229c-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="8229c-137">要包含在核准要求中以連結至私人連結的自訂訊息</span><span class="sxs-lookup"><span data-stu-id="8229c-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="8229c-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="8229c-139">私人連結資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8229c-139">The Location of Private Link resource.</span></span> <span data-ttu-id="8229c-140">設定 PrivateLinkResourceId 時，位置為必填專案</span><span class="sxs-lookup"><span data-stu-id="8229c-140">Location is required when PrivateLinkResourceId is set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8229c-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8229c-142">私人連結的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8229c-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="8229c-143">填上此選擇性欄位表示此後端為'私人'</span><span class="sxs-lookup"><span data-stu-id="8229c-143">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-144">-重量</span><span class="sxs-lookup"><span data-stu-id="8229c-144">-Weight</span></span>
<span data-ttu-id="8229c-145">為了達到負載平衡的目的，此端點的粗細。</span><span class="sxs-lookup"><span data-stu-id="8229c-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="8229c-146">必須介於 1 到 1000 之間。</span><span class="sxs-lookup"><span data-stu-id="8229c-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="8229c-147">預設值為 50</span><span class="sxs-lookup"><span data-stu-id="8229c-147">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8229c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8229c-148">CommonParameters</span></span>
<span data-ttu-id="8229c-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8229c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8229c-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8229c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8229c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8229c-151">INPUTS</span></span>

### <span data-ttu-id="8229c-152">沒有</span><span class="sxs-lookup"><span data-stu-id="8229c-152">None</span></span>

## <span data-ttu-id="8229c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8229c-153">OUTPUTS</span></span>

### <span data-ttu-id="8229c-154">Microsoft.Azure.Commands.FrontDoor.models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="8229c-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="8229c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8229c-155">NOTES</span></span>

## <span data-ttu-id="8229c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8229c-156">RELATED LINKS</span></span>

[<span data-ttu-id="8229c-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="8229c-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
