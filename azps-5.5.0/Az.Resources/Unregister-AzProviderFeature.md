---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128363"
---
# <span data-ttu-id="38c2e-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="38c2e-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="38c2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="38c2e-103">在您的帳戶中登出 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="38c2e-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="38c2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="38c2e-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="38c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="38c2e-106">**AzProviderFeature** Cmdlet 會在您的帳戶中取消註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="38c2e-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="38c2e-107">示例</span><span class="sxs-lookup"><span data-stu-id="38c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="38c2e-108">範例1：登出功能</span><span class="sxs-lookup"><span data-stu-id="38c2e-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="38c2e-109">這會從您的帳戶中登出 AllowApplicationSecurityGroups 的網路功能。</span><span class="sxs-lookup"><span data-stu-id="38c2e-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="38c2e-110">參數</span><span class="sxs-lookup"><span data-stu-id="38c2e-110">PARAMETERS</span></span>

### <span data-ttu-id="38c2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c2e-111">-DefaultProfile</span></span>
<span data-ttu-id="38c2e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38c2e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c2e-113">-功能</span><span class="sxs-lookup"><span data-stu-id="38c2e-113">-FeatureName</span></span>
<span data-ttu-id="38c2e-114">功能名稱。</span><span class="sxs-lookup"><span data-stu-id="38c2e-114">The feature name.</span></span>

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

### <span data-ttu-id="38c2e-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="38c2e-115">-ProviderNamespace</span></span>
<span data-ttu-id="38c2e-116">資源提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="38c2e-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="38c2e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="38c2e-117">-Confirm</span></span>
<span data-ttu-id="38c2e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38c2e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c2e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c2e-119">-WhatIf</span></span>
<span data-ttu-id="38c2e-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38c2e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c2e-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38c2e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c2e-122">CommonParameters</span></span>
<span data-ttu-id="38c2e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38c2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c2e-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38c2e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c2e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="38c2e-125">INPUTS</span></span>

### <span data-ttu-id="38c2e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="38c2e-126">System.String</span></span>

## <span data-ttu-id="38c2e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="38c2e-127">OUTPUTS</span></span>

### <span data-ttu-id="38c2e-128">PSProviderFeature 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="38c2e-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="38c2e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="38c2e-129">NOTES</span></span>

## <span data-ttu-id="38c2e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="38c2e-130">RELATED LINKS</span></span>