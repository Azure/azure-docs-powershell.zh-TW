---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275783"
---
# <span data-ttu-id="9e940-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9e940-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="9e940-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e940-102">SYNOPSIS</span></span>
<span data-ttu-id="9e940-103">移除現有的操作。</span><span class="sxs-lookup"><span data-stu-id="9e940-103">Removes an existing operation.</span></span>

## <span data-ttu-id="9e940-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e940-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e940-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e940-105">DESCRIPTION</span></span>
<span data-ttu-id="9e940-106">AzApiManagementOperation Cmdlet 會移除現有 **的** 操作。</span><span class="sxs-lookup"><span data-stu-id="9e940-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="9e940-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e940-107">EXAMPLES</span></span>

### <span data-ttu-id="9e940-108">範例1：移除現有的 API 操作</span><span class="sxs-lookup"><span data-stu-id="9e940-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="9e940-109">這個命令會移除現有的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="9e940-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="9e940-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e940-110">PARAMETERS</span></span>

### <span data-ttu-id="9e940-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9e940-111">-ApiId</span></span>
<span data-ttu-id="9e940-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e940-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="9e940-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9e940-113">-ApiRevision</span></span>
<span data-ttu-id="9e940-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e940-114">Identifier of API Revision.</span></span> <span data-ttu-id="9e940-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9e940-115">This parameter is optional.</span></span> <span data-ttu-id="9e940-116">如果未指定，將會從目前使用中的 api 修訂中移除該作業。</span><span class="sxs-lookup"><span data-stu-id="9e940-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="9e940-117">-內容</span><span class="sxs-lookup"><span data-stu-id="9e940-117">-Context</span></span>
<span data-ttu-id="9e940-118">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="9e940-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="9e940-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e940-119">-DefaultProfile</span></span>
<span data-ttu-id="9e940-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e940-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e940-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9e940-121">-OperationId</span></span>
<span data-ttu-id="9e940-122">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e940-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="9e940-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e940-123">-PassThru</span></span>
<span data-ttu-id="9e940-124">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="9e940-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9e940-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9e940-125">-Confirm</span></span>
<span data-ttu-id="9e940-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e940-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e940-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e940-127">-WhatIf</span></span>
<span data-ttu-id="9e940-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e940-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e940-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e940-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e940-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e940-130">CommonParameters</span></span>
<span data-ttu-id="9e940-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e940-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e940-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e940-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e940-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9e940-133">INPUTS</span></span>

### <span data-ttu-id="9e940-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e940-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e940-135">System.object</span><span class="sxs-lookup"><span data-stu-id="9e940-135">System.String</span></span>

### <span data-ttu-id="9e940-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9e940-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e940-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9e940-137">OUTPUTS</span></span>

### <span data-ttu-id="9e940-138">System.object</span><span class="sxs-lookup"><span data-stu-id="9e940-138">System.Boolean</span></span>

## <span data-ttu-id="9e940-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9e940-139">NOTES</span></span>

## <span data-ttu-id="9e940-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e940-140">RELATED LINKS</span></span>

[<span data-ttu-id="9e940-141">AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9e940-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="9e940-142">新-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9e940-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="9e940-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9e940-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


