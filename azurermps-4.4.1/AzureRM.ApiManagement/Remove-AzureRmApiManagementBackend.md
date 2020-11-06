---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447201"
---
# <span data-ttu-id="2e698-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2e698-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="2e698-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e698-102">SYNOPSIS</span></span>
<span data-ttu-id="2e698-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="2e698-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e698-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e698-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e698-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e698-105">DESCRIPTION</span></span>
<span data-ttu-id="2e698-106">從 Api 管理移除識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="2e698-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="2e698-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e698-107">EXAMPLES</span></span>

### <span data-ttu-id="2e698-108">範例1：移除後123</span><span class="sxs-lookup"><span data-stu-id="2e698-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="2e698-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e698-109">PARAMETERS</span></span>

### <span data-ttu-id="2e698-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2e698-110">-BackendId</span></span>
<span data-ttu-id="2e698-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e698-111">Identifier of existing backend.</span></span>
<span data-ttu-id="2e698-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2e698-112">This parameter is required.</span></span>

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

### <span data-ttu-id="2e698-113">-內容</span><span class="sxs-lookup"><span data-stu-id="2e698-113">-Context</span></span>
<span data-ttu-id="2e698-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="2e698-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e698-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2e698-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e698-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e698-116">-PassThru</span></span>
<span data-ttu-id="2e698-117">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="2e698-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2e698-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2e698-118">This parameter is optional.</span></span>
<span data-ttu-id="2e698-119">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="2e698-119">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e698-120">-確認</span><span class="sxs-lookup"><span data-stu-id="2e698-120">-Confirm</span></span>
<span data-ttu-id="2e698-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e698-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e698-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e698-122">-WhatIf</span></span>
<span data-ttu-id="2e698-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e698-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e698-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e698-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e698-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e698-125">-DefaultProfile</span></span>
<span data-ttu-id="2e698-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e698-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e698-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e698-127">CommonParameters</span></span>
<span data-ttu-id="2e698-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e698-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e698-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e698-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e698-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2e698-130">INPUTS</span></span>

## <span data-ttu-id="2e698-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2e698-131">OUTPUTS</span></span>

### <span data-ttu-id="2e698-132">bool</span><span class="sxs-lookup"><span data-stu-id="2e698-132">bool</span></span>

## <span data-ttu-id="2e698-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2e698-133">NOTES</span></span>

## <span data-ttu-id="2e698-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e698-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e698-135">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2e698-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="2e698-136">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2e698-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2e698-137">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2e698-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="2e698-138">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2e698-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2e698-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2e698-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
