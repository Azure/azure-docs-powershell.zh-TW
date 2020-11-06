---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 135dced6c66f1212f172a2c435a7468b16e71708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444108"
---
# <span data-ttu-id="91674-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="91674-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="91674-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91674-102">SYNOPSIS</span></span>
<span data-ttu-id="91674-103">移除 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="91674-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91674-104">句法</span><span class="sxs-lookup"><span data-stu-id="91674-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91674-105">說明</span><span class="sxs-lookup"><span data-stu-id="91674-105">DESCRIPTION</span></span>
<span data-ttu-id="91674-106">**AzureRmApiManagementLogger** Cmdlet 會移除 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="91674-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="91674-107">示例</span><span class="sxs-lookup"><span data-stu-id="91674-107">EXAMPLES</span></span>

### <span data-ttu-id="91674-108">範例1：移除記錄器</span><span class="sxs-lookup"><span data-stu-id="91674-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="91674-109">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="91674-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="91674-110">參數</span><span class="sxs-lookup"><span data-stu-id="91674-110">PARAMETERS</span></span>

### <span data-ttu-id="91674-111">-內容</span><span class="sxs-lookup"><span data-stu-id="91674-111">-Context</span></span>
<span data-ttu-id="91674-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="91674-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="91674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91674-113">-DefaultProfile</span></span>
<span data-ttu-id="91674-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91674-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91674-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="91674-115">-LoggerId</span></span>
<span data-ttu-id="91674-116">指定要移除的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="91674-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="91674-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91674-117">-PassThru</span></span>
<span data-ttu-id="91674-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="91674-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="91674-119">-確認</span><span class="sxs-lookup"><span data-stu-id="91674-119">-Confirm</span></span>
<span data-ttu-id="91674-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91674-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91674-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91674-121">-WhatIf</span></span>
<span data-ttu-id="91674-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91674-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91674-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91674-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91674-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91674-124">CommonParameters</span></span>
<span data-ttu-id="91674-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91674-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91674-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91674-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91674-127">輸入</span><span class="sxs-lookup"><span data-stu-id="91674-127">INPUTS</span></span>

### <span data-ttu-id="91674-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="91674-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91674-129">System.object</span><span class="sxs-lookup"><span data-stu-id="91674-129">System.String</span></span>

### <span data-ttu-id="91674-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="91674-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="91674-131">輸出</span><span class="sxs-lookup"><span data-stu-id="91674-131">OUTPUTS</span></span>

### <span data-ttu-id="91674-132">System.object</span><span class="sxs-lookup"><span data-stu-id="91674-132">System.Boolean</span></span>

## <span data-ttu-id="91674-133">筆記</span><span class="sxs-lookup"><span data-stu-id="91674-133">NOTES</span></span>

## <span data-ttu-id="91674-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="91674-134">RELATED LINKS</span></span>

[<span data-ttu-id="91674-135">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="91674-135">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="91674-136">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="91674-136">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="91674-137">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="91674-137">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


