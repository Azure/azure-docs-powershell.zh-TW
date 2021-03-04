---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916514"
---
# <span data-ttu-id="0e07c-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="0e07c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e07c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e07c-103">更新服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="0e07c-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="0e07c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e07c-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e07c-105">描述</span><span class="sxs-lookup"><span data-stu-id="0e07c-105">DESCRIPTION</span></span>
<span data-ttu-id="0e07c-106">**Set-AzServiceEndpointPolicy** Cmdlet 會建立服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="0e07c-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="0e07c-107">例子</span><span class="sxs-lookup"><span data-stu-id="0e07c-107">EXAMPLES</span></span>

### <span data-ttu-id="0e07c-108">範例 1：設定服務端點策略</span><span class="sxs-lookup"><span data-stu-id="0e07c-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="0e07c-109">此命令會更新名為 Policy1 的服務端點策略，其定義物件$serviceEndpointPolicy資源組"resourcegroup1"。</span><span class="sxs-lookup"><span data-stu-id="0e07c-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="0e07c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e07c-110">PARAMETERS</span></span>

### <span data-ttu-id="0e07c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e07c-111">-DefaultProfile</span></span>
<span data-ttu-id="0e07c-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e07c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e07c-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="0e07c-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e07c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="0e07c-115">-Confirm</span></span>
<span data-ttu-id="0e07c-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0e07c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e07c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e07c-117">-WhatIf</span></span>
<span data-ttu-id="0e07c-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e07c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e07c-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e07c-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e07c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e07c-120">CommonParameters</span></span>
<span data-ttu-id="0e07c-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e07c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e07c-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0e07c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e07c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0e07c-123">INPUTS</span></span>

### <span data-ttu-id="0e07c-124">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0e07c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0e07c-125">OUTPUTS</span></span>

### <span data-ttu-id="0e07c-126">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0e07c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0e07c-127">NOTES</span></span>

## <span data-ttu-id="0e07c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e07c-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e07c-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0e07c-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0e07c-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e07c-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
