---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969988"
---
# <span data-ttu-id="8c4ec-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8c4ec-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="8c4ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4ec-103">移除 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="8c4ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c4ec-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c4ec-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4ec-106">**AzApiManagementLogger** Cmdlet 會移除 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="8c4ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c4ec-107">EXAMPLES</span></span>

### <span data-ttu-id="8c4ec-108">範例1：移除記錄器</span><span class="sxs-lookup"><span data-stu-id="8c4ec-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="8c4ec-109">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="8c4ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c4ec-110">PARAMETERS</span></span>

### <span data-ttu-id="8c4ec-111">-內容</span><span class="sxs-lookup"><span data-stu-id="8c4ec-111">-Context</span></span>
<span data-ttu-id="8c4ec-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8c4ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4ec-113">-DefaultProfile</span></span>
<span data-ttu-id="8c4ec-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c4ec-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8c4ec-115">-LoggerId</span></span>
<span data-ttu-id="8c4ec-116">指定要移除的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="8c4ec-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c4ec-117">-PassThru</span></span>
<span data-ttu-id="8c4ec-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="8c4ec-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8c4ec-119">-Confirm</span></span>
<span data-ttu-id="8c4ec-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4ec-121">-WhatIf</span></span>
<span data-ttu-id="8c4ec-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4ec-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4ec-124">CommonParameters</span></span>
<span data-ttu-id="8c4ec-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4ec-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c4ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4ec-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8c4ec-127">INPUTS</span></span>

### <span data-ttu-id="8c4ec-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8c4ec-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c4ec-129">System.object</span><span class="sxs-lookup"><span data-stu-id="8c4ec-129">System.String</span></span>

### <span data-ttu-id="8c4ec-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8c4ec-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c4ec-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8c4ec-131">OUTPUTS</span></span>

### <span data-ttu-id="8c4ec-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8c4ec-132">System.Boolean</span></span>

## <span data-ttu-id="8c4ec-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8c4ec-133">NOTES</span></span>

## <span data-ttu-id="8c4ec-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c4ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c4ec-135">AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8c4ec-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="8c4ec-136">新-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8c4ec-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="8c4ec-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8c4ec-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


