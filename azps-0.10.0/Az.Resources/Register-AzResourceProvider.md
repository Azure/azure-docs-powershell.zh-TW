---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 7f9a5089e48da7c49716abe2bdbe710c0cf30e3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795252"
---
# <span data-ttu-id="e24e7-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e24e7-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="e24e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e24e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e24e7-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="e24e7-103">Registers a resource provider.</span></span>

## <span data-ttu-id="e24e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e24e7-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e24e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="e24e7-105">DESCRIPTION</span></span>
<span data-ttu-id="e24e7-106">**AzResourceProvider** Cmdlet 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="e24e7-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="e24e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="e24e7-107">EXAMPLES</span></span>

### <span data-ttu-id="e24e7-108">範例1：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="e24e7-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e24e7-109">這會為您的帳戶註冊 Microsoft. 網路提供者。</span><span class="sxs-lookup"><span data-stu-id="e24e7-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="e24e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e24e7-110">PARAMETERS</span></span>

### <span data-ttu-id="e24e7-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e24e7-111">-ApiVersion</span></span>
<span data-ttu-id="e24e7-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e24e7-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e24e7-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="e24e7-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e24e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24e7-114">-DefaultProfile</span></span>
<span data-ttu-id="e24e7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e24e7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e24e7-116">-預先</span><span class="sxs-lookup"><span data-stu-id="e24e7-116">-Pre</span></span>
<span data-ttu-id="e24e7-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e24e7-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e24e7-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e24e7-118">-ProviderNamespace</span></span>
<span data-ttu-id="e24e7-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e24e7-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e24e7-120">-確認</span><span class="sxs-lookup"><span data-stu-id="e24e7-120">-Confirm</span></span>
<span data-ttu-id="e24e7-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e24e7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24e7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24e7-122">-WhatIf</span></span>
<span data-ttu-id="e24e7-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e24e7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24e7-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e24e7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24e7-125">CommonParameters</span></span>
<span data-ttu-id="e24e7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e24e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24e7-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e24e7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24e7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e24e7-128">INPUTS</span></span>

## <span data-ttu-id="e24e7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e24e7-129">OUTPUTS</span></span>

## <span data-ttu-id="e24e7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e24e7-130">NOTES</span></span>

## <span data-ttu-id="e24e7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e24e7-131">RELATED LINKS</span></span>

[<span data-ttu-id="e24e7-132">AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e24e7-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e24e7-133">取消註冊-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e24e7-133">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


