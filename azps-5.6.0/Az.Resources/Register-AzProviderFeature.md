---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 1ab198fc422cfb0f880f8c1a3dcd860134b4c2c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917930"
---
# <span data-ttu-id="9eaa9-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="9eaa9-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="9eaa9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaa9-103">在您的帳戶中註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="9eaa9-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eaa9-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eaa9-105">描述</span><span class="sxs-lookup"><span data-stu-id="9eaa9-105">DESCRIPTION</span></span>
<span data-ttu-id="9eaa9-106">**Register-AzProviderFeature** Cmdlet 會註冊您帳戶中的 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="9eaa9-107">例子</span><span class="sxs-lookup"><span data-stu-id="9eaa9-107">EXAMPLES</span></span>

### <span data-ttu-id="9eaa9-108">範例 1：註冊功能</span><span class="sxs-lookup"><span data-stu-id="9eaa9-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="9eaa9-109">這會將 Microsoft.Network 的 AllowApplicationSecurityGroups 功能新增到您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="9eaa9-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eaa9-110">PARAMETERS</span></span>

### <span data-ttu-id="9eaa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaa9-111">-DefaultProfile</span></span>
<span data-ttu-id="9eaa9-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9eaa9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eaa9-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="9eaa9-113">-FeatureName</span></span>
<span data-ttu-id="9eaa9-114">指定此 Cmdlet 登錄的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="9eaa9-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9eaa9-115">-ProviderNamespace</span></span>
<span data-ttu-id="9eaa9-116">指定此 Cmdlet 登錄提供者功能之命名空間。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="9eaa9-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9eaa9-117">-Confirm</span></span>
<span data-ttu-id="9eaa9-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eaa9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eaa9-119">-WhatIf</span></span>
<span data-ttu-id="9eaa9-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eaa9-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eaa9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaa9-122">CommonParameters</span></span>
<span data-ttu-id="9eaa9-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eaa9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaa9-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eaa9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaa9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9eaa9-125">INPUTS</span></span>

### <span data-ttu-id="9eaa9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9eaa9-126">System.String</span></span>

## <span data-ttu-id="9eaa9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9eaa9-127">OUTPUTS</span></span>

### <span data-ttu-id="9eaa9-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="9eaa9-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="9eaa9-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9eaa9-129">NOTES</span></span>

## <span data-ttu-id="9eaa9-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eaa9-130">RELATED LINKS</span></span>

[<span data-ttu-id="9eaa9-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="9eaa9-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


