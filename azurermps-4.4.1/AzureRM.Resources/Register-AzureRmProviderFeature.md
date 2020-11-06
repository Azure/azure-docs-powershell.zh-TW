---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452384"
---
# <span data-ttu-id="4b152-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4b152-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="4b152-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b152-102">SYNOPSIS</span></span>
<span data-ttu-id="4b152-103">在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="4b152-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b152-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b152-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b152-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b152-105">DESCRIPTION</span></span>
<span data-ttu-id="4b152-106">**AzureRmProviderFeature** Cmdlet 會在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="4b152-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="4b152-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b152-107">EXAMPLES</span></span>

## <span data-ttu-id="4b152-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b152-108">PARAMETERS</span></span>

### <span data-ttu-id="4b152-109">-功能</span><span class="sxs-lookup"><span data-stu-id="4b152-109">-FeatureName</span></span>
<span data-ttu-id="4b152-110">指定此 Cmdlet 註冊之功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b152-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="4b152-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4b152-111">-ProviderNamespace</span></span>
<span data-ttu-id="4b152-112">指定此 Cmdlet 註冊提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="4b152-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="4b152-113">-確認</span><span class="sxs-lookup"><span data-stu-id="4b152-113">-Confirm</span></span>
<span data-ttu-id="4b152-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b152-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b152-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b152-115">-WhatIf</span></span>
<span data-ttu-id="4b152-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b152-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b152-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b152-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b152-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b152-118">-DefaultProfile</span></span>
<span data-ttu-id="4b152-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b152-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b152-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b152-120">CommonParameters</span></span>
<span data-ttu-id="4b152-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b152-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b152-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b152-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b152-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4b152-123">INPUTS</span></span>

## <span data-ttu-id="4b152-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4b152-124">OUTPUTS</span></span>

### <span data-ttu-id="4b152-125">[System.object]。清單 ' 1 [PSProviderFeature] SdkModels. 命令.]</span><span class="sxs-lookup"><span data-stu-id="4b152-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="4b152-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4b152-126">NOTES</span></span>

## <span data-ttu-id="4b152-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b152-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b152-128">AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4b152-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


