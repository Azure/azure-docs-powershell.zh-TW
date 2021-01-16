---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282408"
---
# <span data-ttu-id="55fcc-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="55fcc-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="55fcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="55fcc-103">檢查 cloudapp.azure.com 區域中的功能變數名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="55fcc-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="55fcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="55fcc-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55fcc-105">說明</span><span class="sxs-lookup"><span data-stu-id="55fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="55fcc-106">檢查 cloudapp.azure.com 區域中的功能變數名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="55fcc-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="55fcc-107">示例</span><span class="sxs-lookup"><span data-stu-id="55fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="55fcc-108">範例1：檢查 contoso.westus.cloudapp.azure.com 是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="55fcc-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="55fcc-109">參數</span><span class="sxs-lookup"><span data-stu-id="55fcc-109">PARAMETERS</span></span>

### <span data-ttu-id="55fcc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fcc-110">-DefaultProfile</span></span>
<span data-ttu-id="55fcc-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55fcc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55fcc-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="55fcc-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="55fcc-113">-位置</span><span class="sxs-lookup"><span data-stu-id="55fcc-113">-Location</span></span>
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

### <span data-ttu-id="55fcc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fcc-114">CommonParameters</span></span>
<span data-ttu-id="55fcc-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55fcc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fcc-116">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55fcc-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fcc-117">輸入</span><span class="sxs-lookup"><span data-stu-id="55fcc-117">INPUTS</span></span>

### <span data-ttu-id="55fcc-118">所有</span><span class="sxs-lookup"><span data-stu-id="55fcc-118">None</span></span>

## <span data-ttu-id="55fcc-119">輸出</span><span class="sxs-lookup"><span data-stu-id="55fcc-119">OUTPUTS</span></span>

### <span data-ttu-id="55fcc-120">System.object</span><span class="sxs-lookup"><span data-stu-id="55fcc-120">System.Boolean</span></span>

## <span data-ttu-id="55fcc-121">筆記</span><span class="sxs-lookup"><span data-stu-id="55fcc-121">NOTES</span></span>

## <span data-ttu-id="55fcc-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="55fcc-122">RELATED LINKS</span></span>
