---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 35a6731848c7695a8c649d344abaf466437a34f9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401569"
---
# <span data-ttu-id="98b0c-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98b0c-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="98b0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="98b0c-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="98b0c-103">Removes a Backend.</span></span>

## <span data-ttu-id="98b0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="98b0c-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b0c-105">描述</span><span class="sxs-lookup"><span data-stu-id="98b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="98b0c-106">從 Api 管理移除由識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="98b0c-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="98b0c-107">例子</span><span class="sxs-lookup"><span data-stu-id="98b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="98b0c-108">範例 1：移除後端 123</span><span class="sxs-lookup"><span data-stu-id="98b0c-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="98b0c-109">參數</span><span class="sxs-lookup"><span data-stu-id="98b0c-109">PARAMETERS</span></span>

### <span data-ttu-id="98b0c-110">-後端Id</span><span class="sxs-lookup"><span data-stu-id="98b0c-110">-BackendId</span></span>
<span data-ttu-id="98b0c-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98b0c-111">Identifier of existing backend.</span></span>
<span data-ttu-id="98b0c-112">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="98b0c-112">This parameter is required.</span></span>

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

### <span data-ttu-id="98b0c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="98b0c-113">-Context</span></span>
<span data-ttu-id="98b0c-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="98b0c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98b0c-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="98b0c-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b0c-116">-DefaultProfile</span></span>
<span data-ttu-id="98b0c-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98b0c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b0c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98b0c-118">-PassThru</span></span>
<span data-ttu-id="98b0c-119">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="98b0c-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="98b0c-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="98b0c-120">This parameter is optional.</span></span>
<span data-ttu-id="98b0c-121">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="98b0c-121">Default value is false.</span></span>

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

### <span data-ttu-id="98b0c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="98b0c-122">-Confirm</span></span>
<span data-ttu-id="98b0c-123">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98b0c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b0c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b0c-124">-WhatIf</span></span>
<span data-ttu-id="98b0c-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98b0c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b0c-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98b0c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b0c-127">CommonParameters</span></span>
<span data-ttu-id="98b0c-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98b0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b0c-129">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98b0c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b0c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="98b0c-130">INPUTS</span></span>

### <span data-ttu-id="98b0c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="98b0c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98b0c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="98b0c-132">System.String</span></span>

### <span data-ttu-id="98b0c-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98b0c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98b0c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="98b0c-134">OUTPUTS</span></span>

### <span data-ttu-id="98b0c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98b0c-135">System.Boolean</span></span>

## <span data-ttu-id="98b0c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="98b0c-136">NOTES</span></span>

## <span data-ttu-id="98b0c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="98b0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="98b0c-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98b0c-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="98b0c-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98b0c-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="98b0c-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="98b0c-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="98b0c-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="98b0c-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="98b0c-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98b0c-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
