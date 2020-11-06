---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446758"
---
# <span data-ttu-id="4c83d-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4c83d-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4c83d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c83d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c83d-103">取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="4c83d-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c83d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c83d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c83d-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c83d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c83d-106">**AzureRmApplicationGatewayAvailableSslOptions** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="4c83d-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4c83d-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c83d-107">EXAMPLES</span></span>

### <span data-ttu-id="4c83d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4c83d-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="4c83d-109">這個命令會傳回 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="4c83d-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4c83d-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c83d-110">PARAMETERS</span></span>

### <span data-ttu-id="4c83d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c83d-111">-DefaultProfile</span></span>
<span data-ttu-id="4c83d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c83d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c83d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c83d-113">CommonParameters</span></span>
<span data-ttu-id="4c83d-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c83d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c83d-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c83d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c83d-116">輸入</span><span class="sxs-lookup"><span data-stu-id="4c83d-116">INPUTS</span></span>

### <span data-ttu-id="4c83d-117">所有</span><span class="sxs-lookup"><span data-stu-id="4c83d-117">None</span></span>

## <span data-ttu-id="4c83d-118">輸出</span><span class="sxs-lookup"><span data-stu-id="4c83d-118">OUTPUTS</span></span>

### <span data-ttu-id="4c83d-119">PSApplicationGatewayAvailableSslOptions 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c83d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4c83d-120">筆記</span><span class="sxs-lookup"><span data-stu-id="4c83d-120">NOTES</span></span>

## <span data-ttu-id="4c83d-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c83d-121">RELATED LINKS</span></span>

