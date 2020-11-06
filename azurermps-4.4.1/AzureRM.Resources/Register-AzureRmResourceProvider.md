---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452375"
---
# <span data-ttu-id="15576-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="15576-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="15576-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15576-102">SYNOPSIS</span></span>
<span data-ttu-id="15576-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="15576-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15576-104">句法</span><span class="sxs-lookup"><span data-stu-id="15576-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15576-105">說明</span><span class="sxs-lookup"><span data-stu-id="15576-105">DESCRIPTION</span></span>
<span data-ttu-id="15576-106">**AzureRmResourceProvider** Cmdlet 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="15576-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="15576-107">示例</span><span class="sxs-lookup"><span data-stu-id="15576-107">EXAMPLES</span></span>

## <span data-ttu-id="15576-108">參數</span><span class="sxs-lookup"><span data-stu-id="15576-108">PARAMETERS</span></span>

### <span data-ttu-id="15576-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="15576-109">-ApiVersion</span></span>
<span data-ttu-id="15576-110">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="15576-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="15576-111">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="15576-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="15576-112">-預先</span><span class="sxs-lookup"><span data-stu-id="15576-112">-Pre</span></span>
<span data-ttu-id="15576-113">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="15576-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="15576-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="15576-114">-ProviderNamespace</span></span>
<span data-ttu-id="15576-115">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="15576-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="15576-116">-確認</span><span class="sxs-lookup"><span data-stu-id="15576-116">-Confirm</span></span>
<span data-ttu-id="15576-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15576-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15576-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15576-118">-WhatIf</span></span>
<span data-ttu-id="15576-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15576-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15576-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15576-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15576-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15576-121">-DefaultProfile</span></span>
<span data-ttu-id="15576-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15576-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15576-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15576-123">CommonParameters</span></span>
<span data-ttu-id="15576-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15576-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15576-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15576-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15576-126">輸入</span><span class="sxs-lookup"><span data-stu-id="15576-126">INPUTS</span></span>

## <span data-ttu-id="15576-127">輸出</span><span class="sxs-lookup"><span data-stu-id="15576-127">OUTPUTS</span></span>

### <span data-ttu-id="15576-128">PSResourceProvider 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="15576-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="15576-129">筆記</span><span class="sxs-lookup"><span data-stu-id="15576-129">NOTES</span></span>

## <span data-ttu-id="15576-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="15576-130">RELATED LINKS</span></span>

[<span data-ttu-id="15576-131">AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="15576-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="15576-132">取消註冊-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="15576-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


