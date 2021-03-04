---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: dbc21a337263bb0e509188d472e4ff984e22322b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901858"
---
# <span data-ttu-id="f0e41-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="f0e41-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="f0e41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0e41-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e41-103">檢查區域中的功能變數名稱cloudapp.azure.com是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="f0e41-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="f0e41-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0e41-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e41-105">描述</span><span class="sxs-lookup"><span data-stu-id="f0e41-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e41-106">檢查區域中的功能變數名稱cloudapp.azure.com是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="f0e41-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="f0e41-107">例子</span><span class="sxs-lookup"><span data-stu-id="f0e41-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e41-108">範例 1：檢查contoso.westus.cloudapp.azure.com是否可用。</span><span class="sxs-lookup"><span data-stu-id="f0e41-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="f0e41-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0e41-109">PARAMETERS</span></span>

### <span data-ttu-id="f0e41-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e41-110">-DefaultProfile</span></span>
<span data-ttu-id="f0e41-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0e41-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0e41-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f0e41-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="f0e41-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f0e41-113">-Location</span></span>
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

### <span data-ttu-id="f0e41-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e41-114">CommonParameters</span></span>
<span data-ttu-id="f0e41-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0e41-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e41-116">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f0e41-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e41-117">輸入</span><span class="sxs-lookup"><span data-stu-id="f0e41-117">INPUTS</span></span>

### <span data-ttu-id="f0e41-118">沒有</span><span class="sxs-lookup"><span data-stu-id="f0e41-118">None</span></span>

## <span data-ttu-id="f0e41-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f0e41-119">OUTPUTS</span></span>

### <span data-ttu-id="f0e41-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0e41-120">System.Boolean</span></span>

## <span data-ttu-id="f0e41-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f0e41-121">NOTES</span></span>

## <span data-ttu-id="f0e41-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0e41-122">RELATED LINKS</span></span>
