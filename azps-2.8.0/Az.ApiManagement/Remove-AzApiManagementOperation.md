---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: b5d52c4fa70312e276851cb3043c7dbd7babdc1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613922"
---
# <span data-ttu-id="20a26-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="20a26-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="20a26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20a26-102">SYNOPSIS</span></span>
<span data-ttu-id="20a26-103">移除現有的操作。</span><span class="sxs-lookup"><span data-stu-id="20a26-103">Removes an existing operation.</span></span>

## <span data-ttu-id="20a26-104">句法</span><span class="sxs-lookup"><span data-stu-id="20a26-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20a26-105">說明</span><span class="sxs-lookup"><span data-stu-id="20a26-105">DESCRIPTION</span></span>
<span data-ttu-id="20a26-106">AzApiManagementOperation Cmdlet 會移除現有 **的** 操作。</span><span class="sxs-lookup"><span data-stu-id="20a26-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="20a26-107">示例</span><span class="sxs-lookup"><span data-stu-id="20a26-107">EXAMPLES</span></span>

### <span data-ttu-id="20a26-108">範例1：移除現有的 API 操作</span><span class="sxs-lookup"><span data-stu-id="20a26-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="20a26-109">這個命令會移除現有的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="20a26-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="20a26-110">參數</span><span class="sxs-lookup"><span data-stu-id="20a26-110">PARAMETERS</span></span>

### <span data-ttu-id="20a26-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="20a26-111">-ApiId</span></span>
<span data-ttu-id="20a26-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a26-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="20a26-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="20a26-113">-ApiRevision</span></span>
<span data-ttu-id="20a26-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a26-114">Identifier of API Revision.</span></span> <span data-ttu-id="20a26-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20a26-115">This parameter is optional.</span></span> <span data-ttu-id="20a26-116">如果未指定，將會從目前使用中的 api 修訂中移除該作業。</span><span class="sxs-lookup"><span data-stu-id="20a26-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="20a26-117">-內容</span><span class="sxs-lookup"><span data-stu-id="20a26-117">-Context</span></span>
<span data-ttu-id="20a26-118">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="20a26-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="20a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a26-119">-DefaultProfile</span></span>
<span data-ttu-id="20a26-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20a26-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a26-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="20a26-121">-OperationId</span></span>
<span data-ttu-id="20a26-122">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20a26-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="20a26-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20a26-123">-PassThru</span></span>
<span data-ttu-id="20a26-124">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="20a26-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="20a26-125">-確認</span><span class="sxs-lookup"><span data-stu-id="20a26-125">-Confirm</span></span>
<span data-ttu-id="20a26-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20a26-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a26-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a26-127">-WhatIf</span></span>
<span data-ttu-id="20a26-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20a26-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a26-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20a26-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a26-130">CommonParameters</span></span>
<span data-ttu-id="20a26-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20a26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a26-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20a26-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a26-133">輸入</span><span class="sxs-lookup"><span data-stu-id="20a26-133">INPUTS</span></span>

### <span data-ttu-id="20a26-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="20a26-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20a26-135">System.object</span><span class="sxs-lookup"><span data-stu-id="20a26-135">System.String</span></span>

### <span data-ttu-id="20a26-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="20a26-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20a26-137">輸出</span><span class="sxs-lookup"><span data-stu-id="20a26-137">OUTPUTS</span></span>

### <span data-ttu-id="20a26-138">System.object</span><span class="sxs-lookup"><span data-stu-id="20a26-138">System.Boolean</span></span>

## <span data-ttu-id="20a26-139">筆記</span><span class="sxs-lookup"><span data-stu-id="20a26-139">NOTES</span></span>

## <span data-ttu-id="20a26-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="20a26-140">RELATED LINKS</span></span>

[<span data-ttu-id="20a26-141">AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="20a26-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="20a26-142">新-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="20a26-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="20a26-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="20a26-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


