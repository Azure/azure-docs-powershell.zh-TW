---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444112"
---
# <span data-ttu-id="bff0f-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bff0f-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="bff0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bff0f-102">SYNOPSIS</span></span>
<span data-ttu-id="bff0f-103">移除現有的操作。</span><span class="sxs-lookup"><span data-stu-id="bff0f-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bff0f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bff0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bff0f-105">DESCRIPTION</span></span>
<span data-ttu-id="bff0f-106">AzureRmApiManagementOperation Cmdlet 會移除現有 **的** 操作。</span><span class="sxs-lookup"><span data-stu-id="bff0f-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="bff0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="bff0f-107">EXAMPLES</span></span>

### <span data-ttu-id="bff0f-108">範例1：移除現有的 API 操作</span><span class="sxs-lookup"><span data-stu-id="bff0f-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="bff0f-109">這個命令會移除現有的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="bff0f-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="bff0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="bff0f-110">PARAMETERS</span></span>

### <span data-ttu-id="bff0f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bff0f-111">-ApiId</span></span>
<span data-ttu-id="bff0f-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bff0f-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="bff0f-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bff0f-113">-ApiRevision</span></span>
<span data-ttu-id="bff0f-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bff0f-114">Identifier of API Revision.</span></span> <span data-ttu-id="bff0f-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="bff0f-115">This parameter is optional.</span></span> <span data-ttu-id="bff0f-116">如果未指定，將會從目前使用中的 api 修訂中移除該作業。</span><span class="sxs-lookup"><span data-stu-id="bff0f-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="bff0f-117">-內容</span><span class="sxs-lookup"><span data-stu-id="bff0f-117">-Context</span></span>
<span data-ttu-id="bff0f-118">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="bff0f-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bff0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff0f-119">-DefaultProfile</span></span>
<span data-ttu-id="bff0f-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bff0f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff0f-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bff0f-121">-OperationId</span></span>
<span data-ttu-id="bff0f-122">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bff0f-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="bff0f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bff0f-123">-PassThru</span></span>
<span data-ttu-id="bff0f-124">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="bff0f-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="bff0f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="bff0f-125">-Confirm</span></span>
<span data-ttu-id="bff0f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bff0f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff0f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff0f-127">-WhatIf</span></span>
<span data-ttu-id="bff0f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bff0f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff0f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bff0f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff0f-130">CommonParameters</span></span>
<span data-ttu-id="bff0f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bff0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff0f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bff0f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff0f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="bff0f-133">INPUTS</span></span>

### <span data-ttu-id="bff0f-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bff0f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bff0f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="bff0f-135">System.String</span></span>

### <span data-ttu-id="bff0f-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="bff0f-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bff0f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bff0f-137">OUTPUTS</span></span>

### <span data-ttu-id="bff0f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="bff0f-138">System.Boolean</span></span>

## <span data-ttu-id="bff0f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="bff0f-139">NOTES</span></span>

## <span data-ttu-id="bff0f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="bff0f-140">RELATED LINKS</span></span>

[<span data-ttu-id="bff0f-141">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bff0f-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bff0f-142">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bff0f-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bff0f-143">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bff0f-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)

