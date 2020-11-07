---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794485"
---
# <span data-ttu-id="59c41-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="59c41-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="59c41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59c41-102">SYNOPSIS</span></span>
<span data-ttu-id="59c41-103">取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="59c41-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="59c41-104">句法</span><span class="sxs-lookup"><span data-stu-id="59c41-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59c41-105">說明</span><span class="sxs-lookup"><span data-stu-id="59c41-105">DESCRIPTION</span></span>
<span data-ttu-id="59c41-106">**AzApplicationGatewayAvailableSslOption** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="59c41-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="59c41-107">示例</span><span class="sxs-lookup"><span data-stu-id="59c41-107">EXAMPLES</span></span>

### <span data-ttu-id="59c41-108">範例1</span><span class="sxs-lookup"><span data-stu-id="59c41-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="59c41-109">這個命令會傳回 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="59c41-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="59c41-110">參數</span><span class="sxs-lookup"><span data-stu-id="59c41-110">PARAMETERS</span></span>

### <span data-ttu-id="59c41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c41-111">-DefaultProfile</span></span>
<span data-ttu-id="59c41-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59c41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59c41-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c41-113">CommonParameters</span></span>
<span data-ttu-id="59c41-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59c41-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c41-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59c41-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c41-116">輸入</span><span class="sxs-lookup"><span data-stu-id="59c41-116">INPUTS</span></span>

### <span data-ttu-id="59c41-117">所有</span><span class="sxs-lookup"><span data-stu-id="59c41-117">None</span></span>

## <span data-ttu-id="59c41-118">輸出</span><span class="sxs-lookup"><span data-stu-id="59c41-118">OUTPUTS</span></span>

### <span data-ttu-id="59c41-119">PSApplicationGatewayAvailableSslOptions 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59c41-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="59c41-120">筆記</span><span class="sxs-lookup"><span data-stu-id="59c41-120">NOTES</span></span>

## <span data-ttu-id="59c41-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="59c41-121">RELATED LINKS</span></span>

