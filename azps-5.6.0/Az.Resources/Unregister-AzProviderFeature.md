---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 30c315240cf667db37c6c605cda093fe7811a3ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903789"
---
# <span data-ttu-id="2d731-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="2d731-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="2d731-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d731-102">SYNOPSIS</span></span>
<span data-ttu-id="2d731-103">取消註冊您帳戶中的 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="2d731-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="2d731-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d731-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d731-105">描述</span><span class="sxs-lookup"><span data-stu-id="2d731-105">DESCRIPTION</span></span>
<span data-ttu-id="2d731-106">取消 **註冊-AzProviderFeature Cmdlet** 會取消註冊您帳戶中的 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="2d731-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="2d731-107">例子</span><span class="sxs-lookup"><span data-stu-id="2d731-107">EXAMPLES</span></span>

### <span data-ttu-id="2d731-108">範例 1：取消註冊功能</span><span class="sxs-lookup"><span data-stu-id="2d731-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="2d731-109">這會從您的帳戶取消註冊 Microsoft.Network 的 AllowApplicationSecurityGroups 功能。</span><span class="sxs-lookup"><span data-stu-id="2d731-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="2d731-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d731-110">PARAMETERS</span></span>

### <span data-ttu-id="2d731-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d731-111">-DefaultProfile</span></span>
<span data-ttu-id="2d731-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d731-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d731-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="2d731-113">-FeatureName</span></span>
<span data-ttu-id="2d731-114">功能名稱。</span><span class="sxs-lookup"><span data-stu-id="2d731-114">The feature name.</span></span>

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

### <span data-ttu-id="2d731-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="2d731-115">-ProviderNamespace</span></span>
<span data-ttu-id="2d731-116">資源提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="2d731-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="2d731-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2d731-117">-Confirm</span></span>
<span data-ttu-id="2d731-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d731-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d731-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d731-119">-WhatIf</span></span>
<span data-ttu-id="2d731-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d731-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d731-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d731-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d731-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d731-122">CommonParameters</span></span>
<span data-ttu-id="2d731-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d731-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d731-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d731-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d731-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2d731-125">INPUTS</span></span>

### <span data-ttu-id="2d731-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2d731-126">System.String</span></span>

## <span data-ttu-id="2d731-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2d731-127">OUTPUTS</span></span>

### <span data-ttu-id="2d731-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="2d731-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="2d731-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2d731-129">NOTES</span></span>

## <span data-ttu-id="2d731-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d731-130">RELATED LINKS</span></span>