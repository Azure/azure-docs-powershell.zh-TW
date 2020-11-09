---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288056"
---
# <span data-ttu-id="48c80-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="48c80-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="48c80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48c80-102">SYNOPSIS</span></span>
<span data-ttu-id="48c80-103">在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="48c80-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="48c80-104">句法</span><span class="sxs-lookup"><span data-stu-id="48c80-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c80-105">說明</span><span class="sxs-lookup"><span data-stu-id="48c80-105">DESCRIPTION</span></span>
<span data-ttu-id="48c80-106">**AzProviderFeature** Cmdlet 會在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="48c80-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="48c80-107">示例</span><span class="sxs-lookup"><span data-stu-id="48c80-107">EXAMPLES</span></span>

### <span data-ttu-id="48c80-108">範例1：註冊功能</span><span class="sxs-lookup"><span data-stu-id="48c80-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="48c80-109">這會將 Microsoft 的 AllowApplicationSecurityGroups 功能新增至您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="48c80-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="48c80-110">參數</span><span class="sxs-lookup"><span data-stu-id="48c80-110">PARAMETERS</span></span>

### <span data-ttu-id="48c80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c80-111">-DefaultProfile</span></span>
<span data-ttu-id="48c80-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="48c80-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48c80-113">-功能</span><span class="sxs-lookup"><span data-stu-id="48c80-113">-FeatureName</span></span>
<span data-ttu-id="48c80-114">指定此 Cmdlet 註冊之功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="48c80-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="48c80-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="48c80-115">-ProviderNamespace</span></span>
<span data-ttu-id="48c80-116">指定此 Cmdlet 註冊提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="48c80-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="48c80-117">-確認</span><span class="sxs-lookup"><span data-stu-id="48c80-117">-Confirm</span></span>
<span data-ttu-id="48c80-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48c80-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c80-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c80-119">-WhatIf</span></span>
<span data-ttu-id="48c80-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48c80-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48c80-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48c80-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c80-122">CommonParameters</span></span>
<span data-ttu-id="48c80-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48c80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c80-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48c80-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c80-125">輸入</span><span class="sxs-lookup"><span data-stu-id="48c80-125">INPUTS</span></span>

### <span data-ttu-id="48c80-126">System.object</span><span class="sxs-lookup"><span data-stu-id="48c80-126">System.String</span></span>

## <span data-ttu-id="48c80-127">輸出</span><span class="sxs-lookup"><span data-stu-id="48c80-127">OUTPUTS</span></span>

### <span data-ttu-id="48c80-128">PSProviderFeature 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="48c80-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="48c80-129">筆記</span><span class="sxs-lookup"><span data-stu-id="48c80-129">NOTES</span></span>

## <span data-ttu-id="48c80-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="48c80-130">RELATED LINKS</span></span>

[<span data-ttu-id="48c80-131">AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="48c80-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


