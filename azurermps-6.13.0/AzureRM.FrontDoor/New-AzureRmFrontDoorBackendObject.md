---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624379"
---
# <span data-ttu-id="46b06-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="46b06-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="46b06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46b06-102">SYNOPSIS</span></span>
<span data-ttu-id="46b06-103">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="46b06-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b06-104">句法</span><span class="sxs-lookup"><span data-stu-id="46b06-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b06-105">說明</span><span class="sxs-lookup"><span data-stu-id="46b06-105">DESCRIPTION</span></span>
<span data-ttu-id="46b06-106">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="46b06-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="46b06-107">示例</span><span class="sxs-lookup"><span data-stu-id="46b06-107">EXAMPLES</span></span>

### <span data-ttu-id="46b06-108">範例1</span><span class="sxs-lookup"><span data-stu-id="46b06-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="46b06-109">建立用來建立前門的 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="46b06-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="46b06-110">參數</span><span class="sxs-lookup"><span data-stu-id="46b06-110">PARAMETERS</span></span>

### <span data-ttu-id="46b06-111">-位址</span><span class="sxs-lookup"><span data-stu-id="46b06-111">-Address</span></span>
<span data-ttu-id="46b06-112">後端 (IP 位址或 FQDN) 的位置</span><span class="sxs-lookup"><span data-stu-id="46b06-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="46b06-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="46b06-113">-BackendHostHeader</span></span>
<span data-ttu-id="46b06-114">要用來作為傳送到後端之主機標頭的值。</span><span class="sxs-lookup"><span data-stu-id="46b06-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="46b06-115">預設值為後端位址。</span><span class="sxs-lookup"><span data-stu-id="46b06-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="46b06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b06-116">-DefaultProfile</span></span>
<span data-ttu-id="46b06-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46b06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b06-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="46b06-118">-EnabledState</span></span>
<span data-ttu-id="46b06-119">是否要啟用此後端的使用。</span><span class="sxs-lookup"><span data-stu-id="46b06-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="46b06-120">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="46b06-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="46b06-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="46b06-121">-HttpPort</span></span>
<span data-ttu-id="46b06-122">HTTP TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="46b06-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="46b06-123">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="46b06-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="46b06-124">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="46b06-124">Default value is 80.</span></span>

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

### <span data-ttu-id="46b06-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="46b06-125">-HttpsPort</span></span>
<span data-ttu-id="46b06-126">HTTPS TCP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="46b06-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="46b06-127">必須介於1至65535。</span><span class="sxs-lookup"><span data-stu-id="46b06-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="46b06-128">預設值為443</span><span class="sxs-lookup"><span data-stu-id="46b06-128">Default value is 443</span></span>

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

### <span data-ttu-id="46b06-129">-優先順序</span><span class="sxs-lookup"><span data-stu-id="46b06-129">-Priority</span></span>
<span data-ttu-id="46b06-130">要用於負載平衡的優先順序。</span><span class="sxs-lookup"><span data-stu-id="46b06-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="46b06-131">必須介於1到5。</span><span class="sxs-lookup"><span data-stu-id="46b06-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="46b06-132">預設值為1</span><span class="sxs-lookup"><span data-stu-id="46b06-132">Default value is 1</span></span>

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

### <span data-ttu-id="46b06-133">寬度</span><span class="sxs-lookup"><span data-stu-id="46b06-133">-Weight</span></span>
<span data-ttu-id="46b06-134">用於負載平衡的此端點的權重。</span><span class="sxs-lookup"><span data-stu-id="46b06-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="46b06-135">必須介於1至1000。</span><span class="sxs-lookup"><span data-stu-id="46b06-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="46b06-136">預設值為50</span><span class="sxs-lookup"><span data-stu-id="46b06-136">Default value is 50</span></span>

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

### <span data-ttu-id="46b06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b06-137">CommonParameters</span></span>
<span data-ttu-id="46b06-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46b06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b06-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46b06-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b06-140">輸入</span><span class="sxs-lookup"><span data-stu-id="46b06-140">INPUTS</span></span>

### <span data-ttu-id="46b06-141">所有</span><span class="sxs-lookup"><span data-stu-id="46b06-141">None</span></span>

## <span data-ttu-id="46b06-142">輸出</span><span class="sxs-lookup"><span data-stu-id="46b06-142">OUTPUTS</span></span>

### <span data-ttu-id="46b06-143">PSBackend 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="46b06-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="46b06-144">筆記</span><span class="sxs-lookup"><span data-stu-id="46b06-144">NOTES</span></span>

## <span data-ttu-id="46b06-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="46b06-145">RELATED LINKS</span></span>

[<span data-ttu-id="46b06-146">新-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="46b06-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
