---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446895"
---
# <span data-ttu-id="eff10-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="eff10-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="eff10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eff10-102">SYNOPSIS</span></span>
<span data-ttu-id="eff10-103">移除現有的操作。</span><span class="sxs-lookup"><span data-stu-id="eff10-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff10-104">句法</span><span class="sxs-lookup"><span data-stu-id="eff10-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff10-105">說明</span><span class="sxs-lookup"><span data-stu-id="eff10-105">DESCRIPTION</span></span>
<span data-ttu-id="eff10-106">AzureRmApiManagementOperation Cmdlet 會移除現有 **的** 操作。</span><span class="sxs-lookup"><span data-stu-id="eff10-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="eff10-107">示例</span><span class="sxs-lookup"><span data-stu-id="eff10-107">EXAMPLES</span></span>

### <span data-ttu-id="eff10-108">範例1：移除現有的 API 操作</span><span class="sxs-lookup"><span data-stu-id="eff10-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="eff10-109">這個命令會移除現有的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="eff10-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="eff10-110">參數</span><span class="sxs-lookup"><span data-stu-id="eff10-110">PARAMETERS</span></span>

### <span data-ttu-id="eff10-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="eff10-111">-ApiId</span></span>
<span data-ttu-id="eff10-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eff10-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="eff10-113">-內容</span><span class="sxs-lookup"><span data-stu-id="eff10-113">-Context</span></span>
<span data-ttu-id="eff10-114">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="eff10-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="eff10-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="eff10-115">-OperationId</span></span>
<span data-ttu-id="eff10-116">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eff10-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="eff10-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eff10-117">-PassThru</span></span>
<span data-ttu-id="eff10-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="eff10-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="eff10-119">-確認</span><span class="sxs-lookup"><span data-stu-id="eff10-119">-Confirm</span></span>
<span data-ttu-id="eff10-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eff10-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff10-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff10-121">-WhatIf</span></span>
<span data-ttu-id="eff10-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eff10-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff10-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eff10-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff10-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff10-124">-DefaultProfile</span></span>
<span data-ttu-id="eff10-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eff10-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff10-126">CommonParameters</span></span>
<span data-ttu-id="eff10-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eff10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff10-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eff10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff10-129">輸入</span><span class="sxs-lookup"><span data-stu-id="eff10-129">INPUTS</span></span>

## <span data-ttu-id="eff10-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eff10-130">OUTPUTS</span></span>

### <span data-ttu-id="eff10-131">bool</span><span class="sxs-lookup"><span data-stu-id="eff10-131">bool</span></span>

## <span data-ttu-id="eff10-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eff10-132">NOTES</span></span>

## <span data-ttu-id="eff10-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eff10-133">RELATED LINKS</span></span>

[<span data-ttu-id="eff10-134">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="eff10-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="eff10-135">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="eff10-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="eff10-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="eff10-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


