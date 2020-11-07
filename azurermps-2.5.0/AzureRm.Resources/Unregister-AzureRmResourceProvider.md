---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800674"
---
# <span data-ttu-id="a6984-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a6984-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="a6984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6984-102">SYNOPSIS</span></span>
<span data-ttu-id="a6984-103">登出資源提供者。</span><span class="sxs-lookup"><span data-stu-id="a6984-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6984-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6984-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6984-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6984-105">DESCRIPTION</span></span>
<span data-ttu-id="a6984-106">AzureRmResourceProvider Cmdlet 會 **取消** 註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="a6984-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="a6984-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6984-107">EXAMPLES</span></span>

## <span data-ttu-id="a6984-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6984-108">PARAMETERS</span></span>

### <span data-ttu-id="a6984-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a6984-109">-ApiVersion</span></span>
<span data-ttu-id="a6984-110">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a6984-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a6984-111">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="a6984-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a6984-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6984-112">-DefaultProfile</span></span>
<span data-ttu-id="a6984-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a6984-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6984-114">-預先</span><span class="sxs-lookup"><span data-stu-id="a6984-114">-Pre</span></span>
<span data-ttu-id="a6984-115">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a6984-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a6984-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a6984-116">-ProviderNamespace</span></span>
<span data-ttu-id="a6984-117">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="a6984-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="a6984-118">-確認</span><span class="sxs-lookup"><span data-stu-id="a6984-118">-Confirm</span></span>
<span data-ttu-id="a6984-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6984-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6984-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6984-120">-WhatIf</span></span>
<span data-ttu-id="a6984-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6984-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6984-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6984-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6984-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6984-123">CommonParameters</span></span>
<span data-ttu-id="a6984-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6984-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6984-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6984-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6984-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a6984-126">INPUTS</span></span>

## <span data-ttu-id="a6984-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a6984-127">OUTPUTS</span></span>

## <span data-ttu-id="a6984-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a6984-128">NOTES</span></span>

## <span data-ttu-id="a6984-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6984-129">RELATED LINKS</span></span>

[<span data-ttu-id="a6984-130">AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a6984-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="a6984-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a6984-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


