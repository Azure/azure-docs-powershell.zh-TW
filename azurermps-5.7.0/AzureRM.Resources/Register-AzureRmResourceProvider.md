---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624672"
---
# <span data-ttu-id="3254e-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3254e-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3254e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3254e-102">SYNOPSIS</span></span>
<span data-ttu-id="3254e-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3254e-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3254e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3254e-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3254e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3254e-105">DESCRIPTION</span></span>
<span data-ttu-id="3254e-106">**AzureRmResourceProvider** Cmdlet 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3254e-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3254e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3254e-107">EXAMPLES</span></span>

### <span data-ttu-id="3254e-108">範例1：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="3254e-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="3254e-109">這會為您的帳戶註冊 Microsoft. 網路提供者。</span><span class="sxs-lookup"><span data-stu-id="3254e-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="3254e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3254e-110">PARAMETERS</span></span>

### <span data-ttu-id="3254e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3254e-111">-ApiVersion</span></span>
<span data-ttu-id="3254e-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3254e-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3254e-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="3254e-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3254e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3254e-114">-DefaultProfile</span></span>
<span data-ttu-id="3254e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3254e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3254e-116">-預先</span><span class="sxs-lookup"><span data-stu-id="3254e-116">-Pre</span></span>
<span data-ttu-id="3254e-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3254e-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3254e-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3254e-118">-ProviderNamespace</span></span>
<span data-ttu-id="3254e-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3254e-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3254e-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3254e-120">-Confirm</span></span>
<span data-ttu-id="3254e-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3254e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3254e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3254e-122">-WhatIf</span></span>
<span data-ttu-id="3254e-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3254e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3254e-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3254e-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3254e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3254e-125">CommonParameters</span></span>
<span data-ttu-id="3254e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3254e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3254e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3254e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3254e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3254e-128">INPUTS</span></span>

### <span data-ttu-id="3254e-129">所有</span><span class="sxs-lookup"><span data-stu-id="3254e-129">None</span></span>
<span data-ttu-id="3254e-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3254e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3254e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3254e-131">OUTPUTS</span></span>

### <span data-ttu-id="3254e-132">PSResourceProvider 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="3254e-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="3254e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3254e-133">NOTES</span></span>

## <span data-ttu-id="3254e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3254e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3254e-135">AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3254e-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="3254e-136">取消註冊-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3254e-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


