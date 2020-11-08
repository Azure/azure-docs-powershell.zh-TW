---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126250"
---
# <span data-ttu-id="0be7c-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0be7c-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="0be7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0be7c-102">SYNOPSIS</span></span>
<span data-ttu-id="0be7c-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="0be7c-103">Registers a resource provider.</span></span>

## <span data-ttu-id="0be7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0be7c-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0be7c-105">DESCRIPTION</span></span>
<span data-ttu-id="0be7c-106">**AzResourceProvider** Cmdlet 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="0be7c-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="0be7c-107">示例</span><span class="sxs-lookup"><span data-stu-id="0be7c-107">EXAMPLES</span></span>

### <span data-ttu-id="0be7c-108">範例1：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="0be7c-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="0be7c-109">這會為您的帳戶註冊 Microsoft. 網路提供者。</span><span class="sxs-lookup"><span data-stu-id="0be7c-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="0be7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0be7c-110">PARAMETERS</span></span>

### <span data-ttu-id="0be7c-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0be7c-111">-ApiVersion</span></span>
<span data-ttu-id="0be7c-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0be7c-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0be7c-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="0be7c-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0be7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be7c-114">-DefaultProfile</span></span>
<span data-ttu-id="0be7c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0be7c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0be7c-116">-預先</span><span class="sxs-lookup"><span data-stu-id="0be7c-116">-Pre</span></span>
<span data-ttu-id="0be7c-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0be7c-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0be7c-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0be7c-118">-ProviderNamespace</span></span>
<span data-ttu-id="0be7c-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="0be7c-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="0be7c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="0be7c-120">-Confirm</span></span>
<span data-ttu-id="0be7c-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0be7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be7c-122">-WhatIf</span></span>
<span data-ttu-id="0be7c-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0be7c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0be7c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0be7c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0be7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be7c-125">CommonParameters</span></span>
<span data-ttu-id="0be7c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0be7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be7c-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0be7c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be7c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0be7c-128">INPUTS</span></span>

### <span data-ttu-id="0be7c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="0be7c-129">System.String</span></span>

## <span data-ttu-id="0be7c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0be7c-130">OUTPUTS</span></span>

### <span data-ttu-id="0be7c-131">PSResourceProvider 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="0be7c-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="0be7c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0be7c-132">NOTES</span></span>

## <span data-ttu-id="0be7c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0be7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0be7c-134">AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0be7c-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="0be7c-135">取消註冊-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0be7c-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


