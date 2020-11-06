---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455160"
---
# <span data-ttu-id="4bbaa-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4bbaa-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="4bbaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbaa-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="4bbaa-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bbaa-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bbaa-105">說明</span><span class="sxs-lookup"><span data-stu-id="4bbaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4bbaa-106">**AzureRmServiceEndpointPolicy** Cmdlet 會移除服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="4bbaa-107">示例</span><span class="sxs-lookup"><span data-stu-id="4bbaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbaa-108">範例1：使用名稱移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="4bbaa-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4bbaa-109">這個命令會移除名稱 Policy1 的服務端點原則，名稱為 "resourcegroup1" 的 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="4bbaa-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="4bbaa-110">範例2：使用輸入物件移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="4bbaa-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4bbaa-111">這個命令會移除屬於名為 "resourcegroup1" 的 resourcegroup 的服務端點原則物件 Policy1</span><span class="sxs-lookup"><span data-stu-id="4bbaa-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="4bbaa-112">參數</span><span class="sxs-lookup"><span data-stu-id="4bbaa-112">PARAMETERS</span></span>

### <span data-ttu-id="4bbaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbaa-113">-DefaultProfile</span></span>
<span data-ttu-id="4bbaa-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bbaa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4bbaa-115">-Force</span></span>
<span data-ttu-id="4bbaa-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="4bbaa-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bbaa-117">-Name</span></span>
<span data-ttu-id="4bbaa-118">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="4bbaa-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bbaa-119">-PassThru</span></span>
<span data-ttu-id="4bbaa-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="4bbaa-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbaa-121">-ResourceGroupName</span></span>
<span data-ttu-id="4bbaa-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4bbaa-123">-Confirm</span></span>
<span data-ttu-id="4bbaa-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbaa-125">-WhatIf</span></span>
<span data-ttu-id="4bbaa-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bbaa-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbaa-128">CommonParameters</span></span>
<span data-ttu-id="4bbaa-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4bbaa-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bbaa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbaa-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4bbaa-131">INPUTS</span></span>

### <span data-ttu-id="4bbaa-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4bbaa-132">System.String</span></span>


## <span data-ttu-id="4bbaa-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4bbaa-133">OUTPUTS</span></span>

### <span data-ttu-id="4bbaa-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4bbaa-134">System.Object</span></span>

## <span data-ttu-id="4bbaa-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4bbaa-135">NOTES</span></span>

## <span data-ttu-id="4bbaa-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bbaa-136">RELATED LINKS</span></span>
