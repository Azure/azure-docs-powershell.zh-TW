---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129521"
---
# <span data-ttu-id="7e73c-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="7e73c-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="7e73c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e73c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e73c-103">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="7e73c-103">Create a PSBackend object</span></span>

## <span data-ttu-id="7e73c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e73c-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e73c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e73c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e73c-106">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="7e73c-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="7e73c-107">示例</span><span class="sxs-lookup"><span data-stu-id="7e73c-107">EXAMPLES</span></span>

### <span data-ttu-id="7e73c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7e73c-108">Example 1</span></span>
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

<span data-ttu-id="7e73c-109">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="7e73c-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="7e73c-110">參數</span><span class="sxs-lookup"><span data-stu-id="7e73c-110">PARAMETERS</span></span>

### <span data-ttu-id="7e73c-111">-位址</span><span class="sxs-lookup"><span data-stu-id="7e73c-111">-Address</span></span>
<span data-ttu-id="7e73c-112">後端 (IP 位址或 FQDN) 的位置</span><span class="sxs-lookup"><span data-stu-id="7e73c-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="7e73c-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="7e73c-113">-BackendHostHeader</span></span>
<span data-ttu-id="7e73c-114">要用來作為傳送到後端之主機標頭的值。</span><span class="sxs-lookup"><span data-stu-id="7e73c-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="7e73c-115">預設值為後端位址。</span><span class="sxs-lookup"><span data-stu-id="7e73c-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="7e73c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e73c-116">-DefaultProfile</span></span>
<span data-ttu-id="7e73c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e73c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e73c-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7e73c-118">-EnabledState</span></span>
<span data-ttu-id="7e73c-119">是否要啟用此後端的使用。</span><span class="sxs-lookup"><span data-stu-id="7e73c-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="7e73c-120">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="7e73c-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="7e73c-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="7e73c-121">-HttpPort</span></span>
<span data-ttu-id="7e73c-122">HTTP TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7e73c-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="7e73c-123">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="7e73c-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="7e73c-124">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="7e73c-124">Default value is 80.</span></span>

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

### <span data-ttu-id="7e73c-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="7e73c-125">-HttpsPort</span></span>
<span data-ttu-id="7e73c-126">HTTPS TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7e73c-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="7e73c-127">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="7e73c-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="7e73c-128">預設值為443</span><span class="sxs-lookup"><span data-stu-id="7e73c-128">Default value is 443</span></span>

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

### <span data-ttu-id="7e73c-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="7e73c-129">-Priority</span></span>
<span data-ttu-id="7e73c-130">要用於負載平衡的優先順序。</span><span class="sxs-lookup"><span data-stu-id="7e73c-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="7e73c-131">必須介於1到5。</span><span class="sxs-lookup"><span data-stu-id="7e73c-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="7e73c-132">預設值為1</span><span class="sxs-lookup"><span data-stu-id="7e73c-132">Default value is 1</span></span>

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

### <span data-ttu-id="7e73c-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="7e73c-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="7e73c-134">私人連結資源的別名。</span><span class="sxs-lookup"><span data-stu-id="7e73c-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="7e73c-135">填入此選用的欄位表示此後端為「私人」</span><span class="sxs-lookup"><span data-stu-id="7e73c-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="7e73c-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="7e73c-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="7e73c-137">要包含在要連線到私人連結之核准要求中的自訂訊息</span><span class="sxs-lookup"><span data-stu-id="7e73c-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="7e73c-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="7e73c-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="7e73c-139">私人連結資源的位置。</span><span class="sxs-lookup"><span data-stu-id="7e73c-139">The Location of Private Link resource.</span></span> <span data-ttu-id="7e73c-140">設定 PrivateLinkResourceId 時，位置是必要的</span><span class="sxs-lookup"><span data-stu-id="7e73c-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="7e73c-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7e73c-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7e73c-142">私人連結的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e73c-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="7e73c-143">填入此選用的欄位表示此後端為「私人」</span><span class="sxs-lookup"><span data-stu-id="7e73c-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="7e73c-144">寬度</span><span class="sxs-lookup"><span data-stu-id="7e73c-144">-Weight</span></span>
<span data-ttu-id="7e73c-145">用於負載平衡的此端點的權重。</span><span class="sxs-lookup"><span data-stu-id="7e73c-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="7e73c-146">必須介於1至1000。</span><span class="sxs-lookup"><span data-stu-id="7e73c-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="7e73c-147">預設值為50</span><span class="sxs-lookup"><span data-stu-id="7e73c-147">Default value is 50</span></span>

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

### <span data-ttu-id="7e73c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e73c-148">CommonParameters</span></span>
<span data-ttu-id="7e73c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e73c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e73c-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7e73c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e73c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="7e73c-151">INPUTS</span></span>

### <span data-ttu-id="7e73c-152">所有</span><span class="sxs-lookup"><span data-stu-id="7e73c-152">None</span></span>

## <span data-ttu-id="7e73c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="7e73c-153">OUTPUTS</span></span>

### <span data-ttu-id="7e73c-154">PSBackend 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="7e73c-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="7e73c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="7e73c-155">NOTES</span></span>

## <span data-ttu-id="7e73c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e73c-156">RELATED LINKS</span></span>

[<span data-ttu-id="7e73c-157">新-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="7e73c-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
