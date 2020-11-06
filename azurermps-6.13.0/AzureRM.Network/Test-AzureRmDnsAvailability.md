---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450214"
---
# <span data-ttu-id="a8322-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="a8322-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="a8322-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8322-102">SYNOPSIS</span></span>
<span data-ttu-id="a8322-103">檢查 cloudapp.azure.com 區域中的功能變數名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="a8322-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8322-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8322-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8322-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8322-105">DESCRIPTION</span></span>
<span data-ttu-id="a8322-106">檢查 cloudapp.azure.com 區域中的功能變數名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="a8322-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="a8322-107">示例</span><span class="sxs-lookup"><span data-stu-id="a8322-107">EXAMPLES</span></span>

### <span data-ttu-id="a8322-108">範例1：檢查 contoso.cloudapp.azure.com 是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="a8322-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="a8322-109">參數</span><span class="sxs-lookup"><span data-stu-id="a8322-109">PARAMETERS</span></span>

### <span data-ttu-id="a8322-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8322-110">-DefaultProfile</span></span>
<span data-ttu-id="a8322-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8322-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8322-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a8322-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8322-113">-位置</span><span class="sxs-lookup"><span data-stu-id="a8322-113">-Location</span></span>
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

### <span data-ttu-id="a8322-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8322-114">CommonParameters</span></span>
<span data-ttu-id="a8322-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8322-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8322-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8322-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8322-117">輸入</span><span class="sxs-lookup"><span data-stu-id="a8322-117">INPUTS</span></span>

### <span data-ttu-id="a8322-118">所有</span><span class="sxs-lookup"><span data-stu-id="a8322-118">None</span></span>

## <span data-ttu-id="a8322-119">輸出</span><span class="sxs-lookup"><span data-stu-id="a8322-119">OUTPUTS</span></span>

### <span data-ttu-id="a8322-120">System.object</span><span class="sxs-lookup"><span data-stu-id="a8322-120">System.Boolean</span></span>

## <span data-ttu-id="a8322-121">筆記</span><span class="sxs-lookup"><span data-stu-id="a8322-121">NOTES</span></span>

## <span data-ttu-id="a8322-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8322-122">RELATED LINKS</span></span>
