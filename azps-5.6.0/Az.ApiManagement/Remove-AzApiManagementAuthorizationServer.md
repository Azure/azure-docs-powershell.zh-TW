---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907173"
---
# <span data-ttu-id="eae5a-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="eae5a-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="eae5a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eae5a-102">SYNOPSIS</span></span>
<span data-ttu-id="eae5a-103">移除授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="eae5a-103">Removes an authorization server.</span></span>

## <span data-ttu-id="eae5a-104">語法</span><span class="sxs-lookup"><span data-stu-id="eae5a-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eae5a-105">描述</span><span class="sxs-lookup"><span data-stu-id="eae5a-105">DESCRIPTION</span></span>
<span data-ttu-id="eae5a-106">**Remove-AzApiManagementAuthorizationServer** Cmdlet 會移除 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="eae5a-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="eae5a-107">例子</span><span class="sxs-lookup"><span data-stu-id="eae5a-107">EXAMPLES</span></span>

### <span data-ttu-id="eae5a-108">範例 1：移除授權伺服器</span><span class="sxs-lookup"><span data-stu-id="eae5a-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="eae5a-109">此命令會移除指定的 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="eae5a-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="eae5a-110">由於 *已指定 Force* 參數，因此不需要確認。</span><span class="sxs-lookup"><span data-stu-id="eae5a-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="eae5a-111">參數</span><span class="sxs-lookup"><span data-stu-id="eae5a-111">PARAMETERS</span></span>

### <span data-ttu-id="eae5a-112">-內容</span><span class="sxs-lookup"><span data-stu-id="eae5a-112">-Context</span></span>
<span data-ttu-id="eae5a-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="eae5a-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eae5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae5a-114">-DefaultProfile</span></span>
<span data-ttu-id="eae5a-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eae5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eae5a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eae5a-116">-PassThru</span></span>
<span data-ttu-id="eae5a-117">Passthru</span><span class="sxs-lookup"><span data-stu-id="eae5a-117">passthru</span></span>

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

### <span data-ttu-id="eae5a-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="eae5a-118">-ServerId</span></span>
<span data-ttu-id="eae5a-119">指定要移除的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="eae5a-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="eae5a-120">-確認</span><span class="sxs-lookup"><span data-stu-id="eae5a-120">-Confirm</span></span>
<span data-ttu-id="eae5a-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eae5a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae5a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae5a-122">-WhatIf</span></span>
<span data-ttu-id="eae5a-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eae5a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eae5a-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eae5a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae5a-125">CommonParameters</span></span>
<span data-ttu-id="eae5a-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eae5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae5a-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eae5a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae5a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eae5a-128">INPUTS</span></span>

### <span data-ttu-id="eae5a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="eae5a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eae5a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eae5a-130">System.String</span></span>

### <span data-ttu-id="eae5a-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eae5a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eae5a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="eae5a-132">OUTPUTS</span></span>

### <span data-ttu-id="eae5a-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eae5a-133">System.Boolean</span></span>

## <span data-ttu-id="eae5a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="eae5a-134">NOTES</span></span>

## <span data-ttu-id="eae5a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="eae5a-135">RELATED LINKS</span></span>

[<span data-ttu-id="eae5a-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="eae5a-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="eae5a-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="eae5a-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="eae5a-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="eae5a-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


