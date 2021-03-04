---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909485"
---
# <span data-ttu-id="f1083-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f1083-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="f1083-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1083-102">SYNOPSIS</span></span>
<span data-ttu-id="f1083-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="f1083-103">Registers a resource provider.</span></span>

## <span data-ttu-id="f1083-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1083-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1083-105">描述</span><span class="sxs-lookup"><span data-stu-id="f1083-105">DESCRIPTION</span></span>
<span data-ttu-id="f1083-106">**Register-AzResourceProvider Cmdlet** 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="f1083-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="f1083-107">例子</span><span class="sxs-lookup"><span data-stu-id="f1083-107">EXAMPLES</span></span>

### <span data-ttu-id="f1083-108">範例 1：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="f1083-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="f1083-109">這會為您的帳戶註冊 Microsoft.Network 提供者。</span><span class="sxs-lookup"><span data-stu-id="f1083-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="f1083-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1083-110">PARAMETERS</span></span>

### <span data-ttu-id="f1083-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f1083-111">-ApiVersion</span></span>
<span data-ttu-id="f1083-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f1083-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f1083-113">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="f1083-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1083-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1083-114">-DefaultProfile</span></span>
<span data-ttu-id="f1083-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f1083-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1083-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1083-116">-Pre</span></span>
<span data-ttu-id="f1083-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f1083-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1083-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f1083-118">-ProviderNamespace</span></span>
<span data-ttu-id="f1083-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f1083-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="f1083-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f1083-120">-Confirm</span></span>
<span data-ttu-id="f1083-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1083-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1083-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1083-122">-WhatIf</span></span>
<span data-ttu-id="f1083-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1083-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1083-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1083-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1083-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1083-125">CommonParameters</span></span>
<span data-ttu-id="f1083-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1083-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1083-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1083-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1083-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f1083-128">INPUTS</span></span>

### <span data-ttu-id="f1083-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f1083-129">System.String</span></span>

## <span data-ttu-id="f1083-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f1083-130">OUTPUTS</span></span>

### <span data-ttu-id="f1083-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f1083-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="f1083-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f1083-132">NOTES</span></span>

## <span data-ttu-id="f1083-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1083-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1083-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f1083-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="f1083-135">取消註冊-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f1083-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


