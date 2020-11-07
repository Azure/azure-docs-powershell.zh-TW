---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626186"
---
# <span data-ttu-id="8c06b-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="8c06b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c06b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c06b-103">移除 API。</span><span class="sxs-lookup"><span data-stu-id="8c06b-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c06b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c06b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c06b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c06b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c06b-106">AzureRmApiManagementApi Cmdlet 會移除現有 **的** API。</span><span class="sxs-lookup"><span data-stu-id="8c06b-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="8c06b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c06b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c06b-108">範例1：移除 API</span><span class="sxs-lookup"><span data-stu-id="8c06b-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="8c06b-109">這個命令會移除具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="8c06b-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="8c06b-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c06b-110">PARAMETERS</span></span>

### <span data-ttu-id="8c06b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8c06b-111">-ApiId</span></span>
<span data-ttu-id="8c06b-112">指定 API 移除的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c06b-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="8c06b-113">-內容</span><span class="sxs-lookup"><span data-stu-id="8c06b-113">-Context</span></span>
<span data-ttu-id="8c06b-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c06b-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c06b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c06b-115">-DefaultProfile</span></span>
<span data-ttu-id="8c06b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c06b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8c06b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c06b-117">-PassThru</span></span>
<span data-ttu-id="8c06b-118">passthru</span><span class="sxs-lookup"><span data-stu-id="8c06b-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c06b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8c06b-119">-Confirm</span></span>
<span data-ttu-id="8c06b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c06b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c06b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c06b-121">-WhatIf</span></span>
<span data-ttu-id="8c06b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c06b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c06b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c06b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c06b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c06b-124">CommonParameters</span></span>
<span data-ttu-id="8c06b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c06b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c06b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c06b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c06b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8c06b-127">INPUTS</span></span>

### <span data-ttu-id="8c06b-128">所有</span><span class="sxs-lookup"><span data-stu-id="8c06b-128">None</span></span>
<span data-ttu-id="8c06b-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8c06b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c06b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8c06b-130">OUTPUTS</span></span>

### <span data-ttu-id="8c06b-131">布林值</span><span class="sxs-lookup"><span data-stu-id="8c06b-131">Boolean</span></span>

## <span data-ttu-id="8c06b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8c06b-132">NOTES</span></span>

## <span data-ttu-id="8c06b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c06b-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c06b-134">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="8c06b-135">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="8c06b-136">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="8c06b-137">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="8c06b-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8c06b-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


