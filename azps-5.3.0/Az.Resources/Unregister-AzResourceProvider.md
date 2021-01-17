---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438627"
---
# <span data-ttu-id="3a4b9-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a4b9-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="3a4b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4b9-103">登出資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="3a4b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a4b9-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4b9-106">AzResourceProvider Cmdlet 會 **取消** 註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="3a4b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="3a4b9-108">範例1：使用 ProviderNamespace 登出資源提供者</span><span class="sxs-lookup"><span data-stu-id="3a4b9-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="3a4b9-109">這個命令會登出資源提供者「Microsoft. 支援」。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="3a4b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a4b9-110">PARAMETERS</span></span>

### <span data-ttu-id="3a4b9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3a4b9-111">-ApiVersion</span></span>
<span data-ttu-id="3a4b9-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3a4b9-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3a4b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4b9-114">-DefaultProfile</span></span>
<span data-ttu-id="3a4b9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3a4b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a4b9-116">-預先</span><span class="sxs-lookup"><span data-stu-id="3a4b9-116">-Pre</span></span>
<span data-ttu-id="3a4b9-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3a4b9-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3a4b9-118">-ProviderNamespace</span></span>
<span data-ttu-id="3a4b9-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3a4b9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3a4b9-120">-Confirm</span></span>
<span data-ttu-id="3a4b9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4b9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4b9-122">-WhatIf</span></span>
<span data-ttu-id="3a4b9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4b9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4b9-125">CommonParameters</span></span>
<span data-ttu-id="3a4b9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4b9-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4b9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3a4b9-128">INPUTS</span></span>

### <span data-ttu-id="3a4b9-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3a4b9-129">System.String</span></span>

## <span data-ttu-id="3a4b9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3a4b9-130">OUTPUTS</span></span>

### <span data-ttu-id="3a4b9-131">PSResourceProvider 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="3a4b9-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="3a4b9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3a4b9-132">NOTES</span></span>

## <span data-ttu-id="3a4b9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a4b9-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a4b9-134">AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a4b9-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="3a4b9-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3a4b9-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


