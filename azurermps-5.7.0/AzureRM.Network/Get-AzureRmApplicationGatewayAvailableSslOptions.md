---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 091170e4cea82184369b3c10c7fd71cb2d326244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449871"
---
# <span data-ttu-id="fd159-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="fd159-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="fd159-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd159-102">SYNOPSIS</span></span>
<span data-ttu-id="fd159-103">取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="fd159-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd159-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd159-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd159-105">說明</span><span class="sxs-lookup"><span data-stu-id="fd159-105">DESCRIPTION</span></span>
<span data-ttu-id="fd159-106">**AzureRmApplicationGatewayAvailableSslOptions** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="fd159-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="fd159-107">示例</span><span class="sxs-lookup"><span data-stu-id="fd159-107">EXAMPLES</span></span>

### <span data-ttu-id="fd159-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fd159-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="fd159-109">這個命令會傳回 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="fd159-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="fd159-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd159-110">PARAMETERS</span></span>

### <span data-ttu-id="fd159-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd159-111">-DefaultProfile</span></span>
<span data-ttu-id="fd159-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd159-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd159-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd159-113">CommonParameters</span></span>
<span data-ttu-id="fd159-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd159-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd159-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd159-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd159-116">輸入</span><span class="sxs-lookup"><span data-stu-id="fd159-116">INPUTS</span></span>

### <span data-ttu-id="fd159-117">所有</span><span class="sxs-lookup"><span data-stu-id="fd159-117">None</span></span>

## <span data-ttu-id="fd159-118">輸出</span><span class="sxs-lookup"><span data-stu-id="fd159-118">OUTPUTS</span></span>

### <span data-ttu-id="fd159-119">PSApplicationGatewayAvailableSslOptions 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fd159-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="fd159-120">筆記</span><span class="sxs-lookup"><span data-stu-id="fd159-120">NOTES</span></span>

## <span data-ttu-id="fd159-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd159-121">RELATED LINKS</span></span>

