---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: 6be1d4f755d11c6c0cbd32488b59f4e141278633
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447254"
---
# <span data-ttu-id="5648c-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5648c-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="5648c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5648c-102">SYNOPSIS</span></span>
<span data-ttu-id="5648c-103">在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="5648c-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5648c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5648c-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5648c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5648c-105">DESCRIPTION</span></span>
<span data-ttu-id="5648c-106">**AzureRmProviderFeature** Cmdlet 會在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="5648c-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="5648c-107">示例</span><span class="sxs-lookup"><span data-stu-id="5648c-107">EXAMPLES</span></span>

### <span data-ttu-id="5648c-108">範例1：註冊功能</span><span class="sxs-lookup"><span data-stu-id="5648c-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="5648c-109">這會將 Microsoft 的 AllowApplicationSecurityGroups 功能新增至您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="5648c-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="5648c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5648c-110">PARAMETERS</span></span>

### <span data-ttu-id="5648c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5648c-111">-DefaultProfile</span></span>
<span data-ttu-id="5648c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5648c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5648c-113">-功能</span><span class="sxs-lookup"><span data-stu-id="5648c-113">-FeatureName</span></span>
<span data-ttu-id="5648c-114">指定此 Cmdlet 註冊之功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="5648c-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5648c-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5648c-115">-ProviderNamespace</span></span>
<span data-ttu-id="5648c-116">指定此 Cmdlet 註冊提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="5648c-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5648c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5648c-117">-Confirm</span></span>
<span data-ttu-id="5648c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5648c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5648c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5648c-119">-WhatIf</span></span>
<span data-ttu-id="5648c-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5648c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5648c-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5648c-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5648c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5648c-122">CommonParameters</span></span>
<span data-ttu-id="5648c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5648c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5648c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5648c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5648c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5648c-125">INPUTS</span></span>

## <span data-ttu-id="5648c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5648c-126">OUTPUTS</span></span>

## <span data-ttu-id="5648c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5648c-127">NOTES</span></span>

## <span data-ttu-id="5648c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5648c-128">RELATED LINKS</span></span>

[<span data-ttu-id="5648c-129">AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5648c-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


