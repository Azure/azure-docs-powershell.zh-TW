---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446752"
---
# <span data-ttu-id="35375-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="35375-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="35375-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35375-102">SYNOPSIS</span></span>
<span data-ttu-id="35375-103">取得應用程式閘道後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="35375-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35375-104">句法</span><span class="sxs-lookup"><span data-stu-id="35375-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35375-105">說明</span><span class="sxs-lookup"><span data-stu-id="35375-105">DESCRIPTION</span></span>
<span data-ttu-id="35375-106">Get-AzureRmApplicationGatewayBackendHealth Cmdlet 會取得應用程式閘道後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="35375-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="35375-107">示例</span><span class="sxs-lookup"><span data-stu-id="35375-107">EXAMPLES</span></span>

### <span data-ttu-id="35375-108">--------------------------範例1：取得不含展開資源的後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="35375-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
<span data-ttu-id="35375-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="35375-109">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="35375-110">這個命令會取得屬於名為 ResourceGroup01 之資源群組的應用程式閘道的後端健康情況，並將它儲存在 $BackendHealth 變數中。</span><span class="sxs-lookup"><span data-stu-id="35375-110">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="35375-111">--------------------------範例1：取得已展開資源的後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="35375-111">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
<span data-ttu-id="35375-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="35375-112">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="35375-113">這個命令會使用 ApplicationGateway01 名為 ResourceGroup01 的資源群組，並將其儲存在 $BackendHealth 變數中的) 應用程式閘道的展開的資源，來取得後端健康狀態 (。</span><span class="sxs-lookup"><span data-stu-id="35375-113">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="35375-114">參數</span><span class="sxs-lookup"><span data-stu-id="35375-114">PARAMETERS</span></span>

### <span data-ttu-id="35375-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="35375-115">-ExpandResource</span></span>
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

### <span data-ttu-id="35375-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="35375-116">-Name</span></span>
<span data-ttu-id="35375-117">指定此 Cmdlet 所取得之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="35375-117">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="35375-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35375-118">-ResourceGroupName</span></span>
<span data-ttu-id="35375-119">指定包含應用程式閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35375-119">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="35375-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35375-120">-DefaultProfile</span></span>
<span data-ttu-id="35375-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35375-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35375-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35375-122">CommonParameters</span></span>
<span data-ttu-id="35375-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35375-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35375-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35375-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35375-125">輸入</span><span class="sxs-lookup"><span data-stu-id="35375-125">INPUTS</span></span>

### <span data-ttu-id="35375-126">System.object</span><span class="sxs-lookup"><span data-stu-id="35375-126">System.String</span></span>

## <span data-ttu-id="35375-127">輸出</span><span class="sxs-lookup"><span data-stu-id="35375-127">OUTPUTS</span></span>

### <span data-ttu-id="35375-128">PSApplicationGatewayBackendHealth 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="35375-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="35375-129">筆記</span><span class="sxs-lookup"><span data-stu-id="35375-129">NOTES</span></span>
<span data-ttu-id="35375-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="35375-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="35375-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="35375-131">RELATED LINKS</span></span>

[<span data-ttu-id="35375-132">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35375-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

