---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: d5f04c44638f5aa0cfc34ca528d57fca8afe5b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788846"
---
# <span data-ttu-id="646c3-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="646c3-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="646c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="646c3-102">SYNOPSIS</span></span>
<span data-ttu-id="646c3-103">移除 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="646c3-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="646c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="646c3-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="646c3-105">DESCRIPTION</span></span>
<span data-ttu-id="646c3-106">**AzApiManagementLogger** Cmdlet 會移除 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="646c3-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="646c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="646c3-107">EXAMPLES</span></span>

### <span data-ttu-id="646c3-108">範例1：移除記錄器</span><span class="sxs-lookup"><span data-stu-id="646c3-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="646c3-109">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="646c3-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="646c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="646c3-110">PARAMETERS</span></span>

### <span data-ttu-id="646c3-111">-內容</span><span class="sxs-lookup"><span data-stu-id="646c3-111">-Context</span></span>
<span data-ttu-id="646c3-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="646c3-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="646c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646c3-113">-DefaultProfile</span></span>
<span data-ttu-id="646c3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="646c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="646c3-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="646c3-115">-LoggerId</span></span>
<span data-ttu-id="646c3-116">指定要移除的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="646c3-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="646c3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="646c3-117">-PassThru</span></span>
<span data-ttu-id="646c3-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="646c3-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="646c3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="646c3-119">-Confirm</span></span>
<span data-ttu-id="646c3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="646c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646c3-121">-WhatIf</span></span>
<span data-ttu-id="646c3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="646c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="646c3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="646c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646c3-124">CommonParameters</span></span>
<span data-ttu-id="646c3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="646c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646c3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="646c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646c3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="646c3-127">INPUTS</span></span>

### <span data-ttu-id="646c3-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="646c3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="646c3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="646c3-129">System.String</span></span>

### <span data-ttu-id="646c3-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="646c3-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="646c3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="646c3-131">OUTPUTS</span></span>

### <span data-ttu-id="646c3-132">System.object</span><span class="sxs-lookup"><span data-stu-id="646c3-132">System.Boolean</span></span>

## <span data-ttu-id="646c3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="646c3-133">NOTES</span></span>

## <span data-ttu-id="646c3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="646c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="646c3-135">AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="646c3-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="646c3-136">新-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="646c3-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="646c3-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="646c3-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


