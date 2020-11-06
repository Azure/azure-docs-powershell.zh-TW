---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444136"
---
# <span data-ttu-id="f7145-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f7145-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="f7145-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7145-102">SYNOPSIS</span></span>
<span data-ttu-id="f7145-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="f7145-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7145-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7145-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7145-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7145-105">DESCRIPTION</span></span>
<span data-ttu-id="f7145-106">從 Api 管理移除識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="f7145-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="f7145-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7145-107">EXAMPLES</span></span>

### <span data-ttu-id="f7145-108">範例1：移除後123</span><span class="sxs-lookup"><span data-stu-id="f7145-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="f7145-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7145-109">PARAMETERS</span></span>

### <span data-ttu-id="f7145-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="f7145-110">-BackendId</span></span>
<span data-ttu-id="f7145-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7145-111">Identifier of existing backend.</span></span>
<span data-ttu-id="f7145-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f7145-112">This parameter is required.</span></span>

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

### <span data-ttu-id="f7145-113">-內容</span><span class="sxs-lookup"><span data-stu-id="f7145-113">-Context</span></span>
<span data-ttu-id="f7145-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f7145-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f7145-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f7145-115">This parameter is required.</span></span>

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

### <span data-ttu-id="f7145-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7145-116">-DefaultProfile</span></span>
<span data-ttu-id="f7145-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7145-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7145-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7145-118">-PassThru</span></span>
<span data-ttu-id="f7145-119">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="f7145-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f7145-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f7145-120">This parameter is optional.</span></span>
<span data-ttu-id="f7145-121">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="f7145-121">Default value is false.</span></span>

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

### <span data-ttu-id="f7145-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f7145-122">-Confirm</span></span>
<span data-ttu-id="f7145-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7145-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7145-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7145-124">-WhatIf</span></span>
<span data-ttu-id="f7145-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7145-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7145-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7145-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7145-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7145-127">CommonParameters</span></span>
<span data-ttu-id="f7145-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7145-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7145-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7145-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7145-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f7145-130">INPUTS</span></span>

### <span data-ttu-id="f7145-131">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f7145-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7145-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f7145-132">System.String</span></span>

### <span data-ttu-id="f7145-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f7145-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7145-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f7145-134">OUTPUTS</span></span>

### <span data-ttu-id="f7145-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f7145-135">System.Boolean</span></span>

## <span data-ttu-id="f7145-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f7145-136">NOTES</span></span>

## <span data-ttu-id="f7145-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7145-137">RELATED LINKS</span></span>

[<span data-ttu-id="f7145-138">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f7145-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="f7145-139">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f7145-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="f7145-140">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f7145-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="f7145-141">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f7145-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="f7145-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f7145-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
