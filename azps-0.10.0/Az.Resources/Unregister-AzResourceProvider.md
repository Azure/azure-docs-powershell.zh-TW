---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c179ac3657a69b908c605fbaf4d0577b8a77a90f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795182"
---
# <span data-ttu-id="3a810-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a810-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="3a810-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a810-102">SYNOPSIS</span></span>
<span data-ttu-id="3a810-103">登出資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3a810-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="3a810-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a810-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a810-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a810-105">DESCRIPTION</span></span>
<span data-ttu-id="3a810-106">AzResourceProvider Cmdlet 會 **取消** 註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3a810-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="3a810-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a810-107">EXAMPLES</span></span>

## <span data-ttu-id="3a810-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a810-108">PARAMETERS</span></span>

### <span data-ttu-id="3a810-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3a810-109">-ApiVersion</span></span>
<span data-ttu-id="3a810-110">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3a810-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3a810-111">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="3a810-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3a810-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a810-112">-DefaultProfile</span></span>
<span data-ttu-id="3a810-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3a810-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a810-114">-預先</span><span class="sxs-lookup"><span data-stu-id="3a810-114">-Pre</span></span>
<span data-ttu-id="3a810-115">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3a810-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3a810-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3a810-116">-ProviderNamespace</span></span>
<span data-ttu-id="3a810-117">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a810-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3a810-118">-確認</span><span class="sxs-lookup"><span data-stu-id="3a810-118">-Confirm</span></span>
<span data-ttu-id="3a810-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a810-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a810-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a810-120">-WhatIf</span></span>
<span data-ttu-id="3a810-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a810-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a810-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a810-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a810-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a810-123">CommonParameters</span></span>
<span data-ttu-id="3a810-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a810-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a810-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a810-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a810-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3a810-126">INPUTS</span></span>

## <span data-ttu-id="3a810-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3a810-127">OUTPUTS</span></span>

## <span data-ttu-id="3a810-128">筆記</span><span class="sxs-lookup"><span data-stu-id="3a810-128">NOTES</span></span>

## <span data-ttu-id="3a810-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a810-129">RELATED LINKS</span></span>

[<span data-ttu-id="3a810-130">AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a810-130">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="3a810-131">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a810-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


