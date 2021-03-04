---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 0db56d65893c9c003261c2004435c5d231c014f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911793"
---
# <span data-ttu-id="98300-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98300-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="98300-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98300-102">SYNOPSIS</span></span>
<span data-ttu-id="98300-103">移除現有的作業。</span><span class="sxs-lookup"><span data-stu-id="98300-103">Removes an existing operation.</span></span>

## <span data-ttu-id="98300-104">語法</span><span class="sxs-lookup"><span data-stu-id="98300-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98300-105">描述</span><span class="sxs-lookup"><span data-stu-id="98300-105">DESCRIPTION</span></span>
<span data-ttu-id="98300-106">**Remove-AzApiManagementOperation Cmdlet** 會移除現有的作業。</span><span class="sxs-lookup"><span data-stu-id="98300-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="98300-107">例子</span><span class="sxs-lookup"><span data-stu-id="98300-107">EXAMPLES</span></span>

### <span data-ttu-id="98300-108">範例 1：移除現有的 API 作業</span><span class="sxs-lookup"><span data-stu-id="98300-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="98300-109">此命令會移除現有的 API 作業。</span><span class="sxs-lookup"><span data-stu-id="98300-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="98300-110">參數</span><span class="sxs-lookup"><span data-stu-id="98300-110">PARAMETERS</span></span>

### <span data-ttu-id="98300-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="98300-111">-ApiId</span></span>
<span data-ttu-id="98300-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98300-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="98300-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="98300-113">-ApiRevision</span></span>
<span data-ttu-id="98300-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98300-114">Identifier of API Revision.</span></span> <span data-ttu-id="98300-115">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="98300-115">This parameter is optional.</span></span> <span data-ttu-id="98300-116">如果未指定，將會從目前使用中的 Api 修訂中移除作業。</span><span class="sxs-lookup"><span data-stu-id="98300-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98300-117">-內容</span><span class="sxs-lookup"><span data-stu-id="98300-117">-Context</span></span>
<span data-ttu-id="98300-118">指定 **PsApiManagementCoNtext 的實例**。</span><span class="sxs-lookup"><span data-stu-id="98300-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="98300-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98300-119">-DefaultProfile</span></span>
<span data-ttu-id="98300-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98300-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98300-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="98300-121">-OperationId</span></span>
<span data-ttu-id="98300-122">指定 API 作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98300-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="98300-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98300-123">-PassThru</span></span>
<span data-ttu-id="98300-124">表示此 Cmdlet 如果成功，會$True值，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="98300-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="98300-125">-確認</span><span class="sxs-lookup"><span data-stu-id="98300-125">-Confirm</span></span>
<span data-ttu-id="98300-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98300-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98300-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98300-127">-WhatIf</span></span>
<span data-ttu-id="98300-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98300-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98300-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98300-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98300-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98300-130">CommonParameters</span></span>
<span data-ttu-id="98300-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98300-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98300-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98300-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98300-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98300-133">INPUTS</span></span>

### <span data-ttu-id="98300-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="98300-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98300-135">System.String</span><span class="sxs-lookup"><span data-stu-id="98300-135">System.String</span></span>

### <span data-ttu-id="98300-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98300-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98300-137">輸出</span><span class="sxs-lookup"><span data-stu-id="98300-137">OUTPUTS</span></span>

### <span data-ttu-id="98300-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98300-138">System.Boolean</span></span>

## <span data-ttu-id="98300-139">筆記</span><span class="sxs-lookup"><span data-stu-id="98300-139">NOTES</span></span>

## <span data-ttu-id="98300-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="98300-140">RELATED LINKS</span></span>

[<span data-ttu-id="98300-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98300-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="98300-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98300-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="98300-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98300-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


