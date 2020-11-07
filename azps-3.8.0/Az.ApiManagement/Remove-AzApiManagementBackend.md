---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: d1a353e9534cbfd2530bb67f5eeda92fbb6d72ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958953"
---
# <span data-ttu-id="669c5-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="669c5-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="669c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="669c5-102">SYNOPSIS</span></span>
<span data-ttu-id="669c5-103">移除後端。</span><span class="sxs-lookup"><span data-stu-id="669c5-103">Removes a Backend.</span></span>

## <span data-ttu-id="669c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="669c5-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="669c5-105">DESCRIPTION</span></span>
<span data-ttu-id="669c5-106">從 Api 管理移除識別碼指定的後端。</span><span class="sxs-lookup"><span data-stu-id="669c5-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="669c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="669c5-107">EXAMPLES</span></span>

### <span data-ttu-id="669c5-108">範例1：移除後123</span><span class="sxs-lookup"><span data-stu-id="669c5-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="669c5-109">參數</span><span class="sxs-lookup"><span data-stu-id="669c5-109">PARAMETERS</span></span>

### <span data-ttu-id="669c5-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="669c5-110">-BackendId</span></span>
<span data-ttu-id="669c5-111">現有後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="669c5-111">Identifier of existing backend.</span></span>
<span data-ttu-id="669c5-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="669c5-112">This parameter is required.</span></span>

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

### <span data-ttu-id="669c5-113">-內容</span><span class="sxs-lookup"><span data-stu-id="669c5-113">-Context</span></span>
<span data-ttu-id="669c5-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="669c5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="669c5-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="669c5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="669c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669c5-116">-DefaultProfile</span></span>
<span data-ttu-id="669c5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="669c5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="669c5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="669c5-118">-PassThru</span></span>
<span data-ttu-id="669c5-119">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="669c5-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="669c5-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="669c5-120">This parameter is optional.</span></span>
<span data-ttu-id="669c5-121">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="669c5-121">Default value is false.</span></span>

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

### <span data-ttu-id="669c5-122">-確認</span><span class="sxs-lookup"><span data-stu-id="669c5-122">-Confirm</span></span>
<span data-ttu-id="669c5-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="669c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669c5-124">-WhatIf</span></span>
<span data-ttu-id="669c5-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="669c5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="669c5-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="669c5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669c5-127">CommonParameters</span></span>
<span data-ttu-id="669c5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="669c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669c5-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="669c5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669c5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="669c5-130">INPUTS</span></span>

### <span data-ttu-id="669c5-131">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="669c5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="669c5-132">System.object</span><span class="sxs-lookup"><span data-stu-id="669c5-132">System.String</span></span>

### <span data-ttu-id="669c5-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="669c5-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="669c5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="669c5-134">OUTPUTS</span></span>

### <span data-ttu-id="669c5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="669c5-135">System.Boolean</span></span>

## <span data-ttu-id="669c5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="669c5-136">NOTES</span></span>

## <span data-ttu-id="669c5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="669c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="669c5-138">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="669c5-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="669c5-139">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="669c5-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="669c5-140">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="669c5-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="669c5-141">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="669c5-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="669c5-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="669c5-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
