---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624371"
---
# <span data-ttu-id="04cbc-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="04cbc-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="04cbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="04cbc-103">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="04cbc-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04cbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="04cbc-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04cbc-105">說明</span><span class="sxs-lookup"><span data-stu-id="04cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="04cbc-106">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="04cbc-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="04cbc-107">示例</span><span class="sxs-lookup"><span data-stu-id="04cbc-107">EXAMPLES</span></span>

### <span data-ttu-id="04cbc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="04cbc-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="04cbc-109">參數</span><span class="sxs-lookup"><span data-stu-id="04cbc-109">PARAMETERS</span></span>

### <span data-ttu-id="04cbc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cbc-110">-DefaultProfile</span></span>
<span data-ttu-id="04cbc-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04cbc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04cbc-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="04cbc-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cbc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cbc-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="04cbc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cbc-114">CommonParameters</span></span>
<span data-ttu-id="04cbc-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04cbc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cbc-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04cbc-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cbc-117">輸入</span><span class="sxs-lookup"><span data-stu-id="04cbc-117">INPUTS</span></span>

### <span data-ttu-id="04cbc-118">System.object</span><span class="sxs-lookup"><span data-stu-id="04cbc-118">System.String</span></span>

## <span data-ttu-id="04cbc-119">輸出</span><span class="sxs-lookup"><span data-stu-id="04cbc-119">OUTPUTS</span></span>

### <span data-ttu-id="04cbc-120">System.object</span><span class="sxs-lookup"><span data-stu-id="04cbc-120">System.String</span></span>

## <span data-ttu-id="04cbc-121">筆記</span><span class="sxs-lookup"><span data-stu-id="04cbc-121">NOTES</span></span>

## <span data-ttu-id="04cbc-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="04cbc-122">RELATED LINKS</span></span>
