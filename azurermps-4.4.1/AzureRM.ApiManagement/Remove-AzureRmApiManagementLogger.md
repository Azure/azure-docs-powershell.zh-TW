---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447194"
---
# <span data-ttu-id="fe945-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fe945-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="fe945-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe945-102">SYNOPSIS</span></span>
<span data-ttu-id="fe945-103">移除 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="fe945-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe945-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe945-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe945-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe945-105">DESCRIPTION</span></span>
<span data-ttu-id="fe945-106">**AzureRmApiManagementLogger** Cmdlet 會移除 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="fe945-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="fe945-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe945-107">EXAMPLES</span></span>

### <span data-ttu-id="fe945-108">範例1：移除記錄器</span><span class="sxs-lookup"><span data-stu-id="fe945-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="fe945-109">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="fe945-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="fe945-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe945-110">PARAMETERS</span></span>

### <span data-ttu-id="fe945-111">-內容</span><span class="sxs-lookup"><span data-stu-id="fe945-111">-Context</span></span>
<span data-ttu-id="fe945-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe945-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe945-113">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="fe945-113">-LoggerId</span></span>
<span data-ttu-id="fe945-114">指定要移除的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe945-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="fe945-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe945-115">-PassThru</span></span>
<span data-ttu-id="fe945-116">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="fe945-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="fe945-117">-確認</span><span class="sxs-lookup"><span data-stu-id="fe945-117">-Confirm</span></span>
<span data-ttu-id="fe945-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe945-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe945-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe945-119">-WhatIf</span></span>
<span data-ttu-id="fe945-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe945-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe945-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe945-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe945-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe945-122">-DefaultProfile</span></span>
<span data-ttu-id="fe945-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe945-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe945-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe945-124">CommonParameters</span></span>
<span data-ttu-id="fe945-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe945-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe945-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe945-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe945-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fe945-127">INPUTS</span></span>

## <span data-ttu-id="fe945-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fe945-128">OUTPUTS</span></span>

### <span data-ttu-id="fe945-129">布林值</span><span class="sxs-lookup"><span data-stu-id="fe945-129">Boolean</span></span>

## <span data-ttu-id="fe945-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fe945-130">NOTES</span></span>

## <span data-ttu-id="fe945-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe945-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe945-132">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fe945-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fe945-133">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fe945-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fe945-134">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fe945-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


