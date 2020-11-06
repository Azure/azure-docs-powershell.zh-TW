---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449424"
---
# <span data-ttu-id="568e0-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="568e0-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="568e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="568e0-102">SYNOPSIS</span></span>
<span data-ttu-id="568e0-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="568e0-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="568e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="568e0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="568e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="568e0-105">DESCRIPTION</span></span>
<span data-ttu-id="568e0-106">從 Api 管理移除識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="568e0-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="568e0-107">示例</span><span class="sxs-lookup"><span data-stu-id="568e0-107">EXAMPLES</span></span>

### <span data-ttu-id="568e0-108">範例1：移除後123</span><span class="sxs-lookup"><span data-stu-id="568e0-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="568e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="568e0-109">PARAMETERS</span></span>

### <span data-ttu-id="568e0-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="568e0-110">-BackendId</span></span>
<span data-ttu-id="568e0-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="568e0-111">Identifier of existing backend.</span></span>
<span data-ttu-id="568e0-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="568e0-112">This parameter is required.</span></span>

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

### <span data-ttu-id="568e0-113">-內容</span><span class="sxs-lookup"><span data-stu-id="568e0-113">-Context</span></span>
<span data-ttu-id="568e0-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="568e0-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="568e0-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="568e0-115">This parameter is required.</span></span>

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

### <span data-ttu-id="568e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568e0-116">-DefaultProfile</span></span>
<span data-ttu-id="568e0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="568e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="568e0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="568e0-118">-PassThru</span></span>
<span data-ttu-id="568e0-119">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="568e0-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="568e0-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="568e0-120">This parameter is optional.</span></span>
<span data-ttu-id="568e0-121">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="568e0-121">Default value is false.</span></span>

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

### <span data-ttu-id="568e0-122">-確認</span><span class="sxs-lookup"><span data-stu-id="568e0-122">-Confirm</span></span>
<span data-ttu-id="568e0-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="568e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568e0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568e0-124">-WhatIf</span></span>
<span data-ttu-id="568e0-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="568e0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="568e0-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="568e0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="568e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568e0-127">CommonParameters</span></span>
<span data-ttu-id="568e0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="568e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568e0-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="568e0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568e0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="568e0-130">INPUTS</span></span>

### <span data-ttu-id="568e0-131">所有</span><span class="sxs-lookup"><span data-stu-id="568e0-131">None</span></span>
<span data-ttu-id="568e0-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="568e0-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="568e0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="568e0-133">OUTPUTS</span></span>

### <span data-ttu-id="568e0-134">bool</span><span class="sxs-lookup"><span data-stu-id="568e0-134">bool</span></span>

## <span data-ttu-id="568e0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="568e0-135">NOTES</span></span>

## <span data-ttu-id="568e0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="568e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="568e0-137">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="568e0-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="568e0-138">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="568e0-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="568e0-139">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="568e0-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="568e0-140">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="568e0-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="568e0-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="568e0-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
