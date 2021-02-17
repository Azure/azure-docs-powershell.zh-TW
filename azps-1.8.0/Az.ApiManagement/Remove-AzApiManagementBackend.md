---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 0c50d88f05537b7ebfe7e7ed074e4c38dd01a254
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400836"
---
# <span data-ttu-id="d94b3-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d94b3-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="d94b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d94b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d94b3-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="d94b3-103">Removes a Backend.</span></span>

## <span data-ttu-id="d94b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="d94b3-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94b3-105">描述</span><span class="sxs-lookup"><span data-stu-id="d94b3-105">DESCRIPTION</span></span>
<span data-ttu-id="d94b3-106">從 Api 管理移除由識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="d94b3-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d94b3-107">例子</span><span class="sxs-lookup"><span data-stu-id="d94b3-107">EXAMPLES</span></span>

### <span data-ttu-id="d94b3-108">範例 1：移除後端 123</span><span class="sxs-lookup"><span data-stu-id="d94b3-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d94b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="d94b3-109">PARAMETERS</span></span>

### <span data-ttu-id="d94b3-110">-後端Id</span><span class="sxs-lookup"><span data-stu-id="d94b3-110">-BackendId</span></span>
<span data-ttu-id="d94b3-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d94b3-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d94b3-112">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="d94b3-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d94b3-113">-內容</span><span class="sxs-lookup"><span data-stu-id="d94b3-113">-Context</span></span>
<span data-ttu-id="d94b3-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="d94b3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d94b3-115">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="d94b3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d94b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94b3-116">-DefaultProfile</span></span>
<span data-ttu-id="d94b3-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d94b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d94b3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d94b3-118">-PassThru</span></span>
<span data-ttu-id="d94b3-119">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="d94b3-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d94b3-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="d94b3-120">This parameter is optional.</span></span>
<span data-ttu-id="d94b3-121">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="d94b3-121">Default value is false.</span></span>

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

### <span data-ttu-id="d94b3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="d94b3-122">-Confirm</span></span>
<span data-ttu-id="d94b3-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d94b3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94b3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94b3-124">-WhatIf</span></span>
<span data-ttu-id="d94b3-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d94b3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d94b3-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d94b3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94b3-127">CommonParameters</span></span>
<span data-ttu-id="d94b3-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d94b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94b3-129">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d94b3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94b3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d94b3-130">INPUTS</span></span>

### <span data-ttu-id="d94b3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="d94b3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d94b3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d94b3-132">System.String</span></span>

### <span data-ttu-id="d94b3-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d94b3-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d94b3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d94b3-134">OUTPUTS</span></span>

### <span data-ttu-id="d94b3-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d94b3-135">System.Boolean</span></span>

## <span data-ttu-id="d94b3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d94b3-136">NOTES</span></span>

## <span data-ttu-id="d94b3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d94b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="d94b3-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d94b3-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="d94b3-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d94b3-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d94b3-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d94b3-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d94b3-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d94b3-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d94b3-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d94b3-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
