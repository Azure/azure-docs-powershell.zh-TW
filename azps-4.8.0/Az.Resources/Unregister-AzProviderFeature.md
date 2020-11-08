---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126857"
---
# <span data-ttu-id="1dbdb-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="1dbdb-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="1dbdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbdb-103">在您的帳戶中登出 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="1dbdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dbdb-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="1dbdb-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbdb-106">**AzProviderFeature** Cmdlet 會在您的帳戶中取消註冊 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="1dbdb-107">示例</span><span class="sxs-lookup"><span data-stu-id="1dbdb-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbdb-108">範例1：登出功能</span><span class="sxs-lookup"><span data-stu-id="1dbdb-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="1dbdb-109">這會從您的帳戶中登出 AllowApplicationSecurityGroups 的網路功能。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="1dbdb-110">參數</span><span class="sxs-lookup"><span data-stu-id="1dbdb-110">PARAMETERS</span></span>

### <span data-ttu-id="1dbdb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdb-111">-DefaultProfile</span></span>
<span data-ttu-id="1dbdb-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbdb-113">-功能</span><span class="sxs-lookup"><span data-stu-id="1dbdb-113">-FeatureName</span></span>
<span data-ttu-id="1dbdb-114">功能名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-114">The feature name.</span></span>

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

### <span data-ttu-id="1dbdb-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="1dbdb-115">-ProviderNamespace</span></span>
<span data-ttu-id="1dbdb-116">資源提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="1dbdb-117">-確認</span><span class="sxs-lookup"><span data-stu-id="1dbdb-117">-Confirm</span></span>
<span data-ttu-id="1dbdb-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbdb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbdb-119">-WhatIf</span></span>
<span data-ttu-id="1dbdb-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbdb-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbdb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbdb-122">CommonParameters</span></span>
<span data-ttu-id="1dbdb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbdb-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1dbdb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbdb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1dbdb-125">INPUTS</span></span>

### <span data-ttu-id="1dbdb-126">System.object</span><span class="sxs-lookup"><span data-stu-id="1dbdb-126">System.String</span></span>

## <span data-ttu-id="1dbdb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1dbdb-127">OUTPUTS</span></span>

### <span data-ttu-id="1dbdb-128">PSProviderFeature 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="1dbdb-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="1dbdb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1dbdb-129">NOTES</span></span>

## <span data-ttu-id="1dbdb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dbdb-130">RELATED LINKS</span></span>
