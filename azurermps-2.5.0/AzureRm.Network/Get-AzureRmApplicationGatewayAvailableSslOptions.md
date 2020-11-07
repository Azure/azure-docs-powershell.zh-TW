---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800905"
---
# <span data-ttu-id="13e94-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="13e94-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="13e94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13e94-102">SYNOPSIS</span></span>
<span data-ttu-id="13e94-103">取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="13e94-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e94-104">句法</span><span class="sxs-lookup"><span data-stu-id="13e94-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13e94-105">說明</span><span class="sxs-lookup"><span data-stu-id="13e94-105">DESCRIPTION</span></span>
<span data-ttu-id="13e94-106">**AzureRmApplicationGatewayAvailableSslOptions** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="13e94-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="13e94-107">示例</span><span class="sxs-lookup"><span data-stu-id="13e94-107">EXAMPLES</span></span>

### <span data-ttu-id="13e94-108">範例1</span><span class="sxs-lookup"><span data-stu-id="13e94-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="13e94-109">這個命令會傳回 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="13e94-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="13e94-110">參數</span><span class="sxs-lookup"><span data-stu-id="13e94-110">PARAMETERS</span></span>

### <span data-ttu-id="13e94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e94-111">-DefaultProfile</span></span>
<span data-ttu-id="13e94-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13e94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e94-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e94-113">CommonParameters</span></span>
<span data-ttu-id="13e94-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13e94-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e94-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13e94-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e94-116">輸入</span><span class="sxs-lookup"><span data-stu-id="13e94-116">INPUTS</span></span>

### <span data-ttu-id="13e94-117">所有</span><span class="sxs-lookup"><span data-stu-id="13e94-117">None</span></span>

## <span data-ttu-id="13e94-118">輸出</span><span class="sxs-lookup"><span data-stu-id="13e94-118">OUTPUTS</span></span>

### <span data-ttu-id="13e94-119">PSApplicationGatewayAvailableSslOptions 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="13e94-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="13e94-120">筆記</span><span class="sxs-lookup"><span data-stu-id="13e94-120">NOTES</span></span>

## <span data-ttu-id="13e94-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="13e94-121">RELATED LINKS</span></span>

