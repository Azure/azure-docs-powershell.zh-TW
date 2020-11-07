---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787826"
---
# <span data-ttu-id="ad8cd-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="ad8cd-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="ad8cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8cd-103">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="ad8cd-103">Create a PSBackend object</span></span>

## <span data-ttu-id="ad8cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad8cd-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad8cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad8cd-105">DESCRIPTION</span></span>
<span data-ttu-id="ad8cd-106">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="ad8cd-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="ad8cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad8cd-107">EXAMPLES</span></span>

### <span data-ttu-id="ad8cd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ad8cd-108">Example 1</span></span>
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

<span data-ttu-id="ad8cd-109">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="ad8cd-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="ad8cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad8cd-110">PARAMETERS</span></span>

### <span data-ttu-id="ad8cd-111">-位址</span><span class="sxs-lookup"><span data-stu-id="ad8cd-111">-Address</span></span>
<span data-ttu-id="ad8cd-112">後端 (IP 位址或 FQDN) 的位置</span><span class="sxs-lookup"><span data-stu-id="ad8cd-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="ad8cd-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="ad8cd-113">-BackendHostHeader</span></span>
<span data-ttu-id="ad8cd-114">要用來作為傳送到後端之主機標頭的值。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="ad8cd-115">預設值為後端位址。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="ad8cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8cd-116">-DefaultProfile</span></span>
<span data-ttu-id="ad8cd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad8cd-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ad8cd-118">-EnabledState</span></span>
<span data-ttu-id="ad8cd-119">是否要啟用此後端的使用。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="ad8cd-120">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="ad8cd-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="ad8cd-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="ad8cd-121">-HttpPort</span></span>
<span data-ttu-id="ad8cd-122">HTTP TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="ad8cd-123">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="ad8cd-124">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-124">Default value is 80.</span></span>

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

### <span data-ttu-id="ad8cd-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="ad8cd-125">-HttpsPort</span></span>
<span data-ttu-id="ad8cd-126">HTTPS TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="ad8cd-127">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="ad8cd-128">預設值為443</span><span class="sxs-lookup"><span data-stu-id="ad8cd-128">Default value is 443</span></span>

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

### <span data-ttu-id="ad8cd-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="ad8cd-129">-Priority</span></span>
<span data-ttu-id="ad8cd-130">要用於負載平衡的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="ad8cd-131">必須介於1到5。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="ad8cd-132">預設值為1</span><span class="sxs-lookup"><span data-stu-id="ad8cd-132">Default value is 1</span></span>

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

### <span data-ttu-id="ad8cd-133">寬度</span><span class="sxs-lookup"><span data-stu-id="ad8cd-133">-Weight</span></span>
<span data-ttu-id="ad8cd-134">用於負載平衡的此端點的權重。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="ad8cd-135">必須介於1至1000。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="ad8cd-136">預設值為50</span><span class="sxs-lookup"><span data-stu-id="ad8cd-136">Default value is 50</span></span>

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

### <span data-ttu-id="ad8cd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8cd-137">CommonParameters</span></span>
<span data-ttu-id="ad8cd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8cd-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8cd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ad8cd-140">INPUTS</span></span>

### <span data-ttu-id="ad8cd-141">所有</span><span class="sxs-lookup"><span data-stu-id="ad8cd-141">None</span></span>

## <span data-ttu-id="ad8cd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ad8cd-142">OUTPUTS</span></span>

### <span data-ttu-id="ad8cd-143">PSBackend 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="ad8cd-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="ad8cd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ad8cd-144">NOTES</span></span>

## <span data-ttu-id="ad8cd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad8cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="ad8cd-146">新-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="ad8cd-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
