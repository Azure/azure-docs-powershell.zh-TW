---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139031"
---
# <span data-ttu-id="f7340-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7340-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7340-102">SYNOPSIS</span></span>
<span data-ttu-id="f7340-103">更新服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="f7340-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="f7340-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7340-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7340-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7340-105">DESCRIPTION</span></span>
<span data-ttu-id="f7340-106">**AzServiceEndpointPolicy** Cmdlet 會建立服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="f7340-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="f7340-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7340-107">EXAMPLES</span></span>

### <span data-ttu-id="f7340-108">範例1：設定服務端點原則</span><span class="sxs-lookup"><span data-stu-id="f7340-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f7340-109">這個命令會更新物件所定義的名為 Policy1 的服務端點原則，$serviceEndpointPolicy 屬於該 resourcegroup "resourcegroup1"。</span><span class="sxs-lookup"><span data-stu-id="f7340-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="f7340-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7340-110">PARAMETERS</span></span>

### <span data-ttu-id="f7340-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7340-111">-DefaultProfile</span></span>
<span data-ttu-id="f7340-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7340-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7340-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f7340-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f7340-115">-確認</span><span class="sxs-lookup"><span data-stu-id="f7340-115">-Confirm</span></span>
<span data-ttu-id="f7340-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7340-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7340-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7340-117">-WhatIf</span></span>
<span data-ttu-id="f7340-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7340-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7340-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7340-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7340-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7340-120">CommonParameters</span></span>
<span data-ttu-id="f7340-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7340-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7340-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7340-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7340-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f7340-123">INPUTS</span></span>

### <span data-ttu-id="f7340-124">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7340-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7340-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f7340-125">OUTPUTS</span></span>

### <span data-ttu-id="f7340-126">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7340-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7340-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f7340-127">NOTES</span></span>

## <span data-ttu-id="f7340-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7340-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7340-129">AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7340-130">新-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7340-131">移除-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7340-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
