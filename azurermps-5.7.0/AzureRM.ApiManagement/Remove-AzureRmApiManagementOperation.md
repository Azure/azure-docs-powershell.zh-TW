---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454784"
---
# <span data-ttu-id="1cb81-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="1cb81-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="1cb81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cb81-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb81-103">移除現有的操作。</span><span class="sxs-lookup"><span data-stu-id="1cb81-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cb81-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cb81-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb81-105">說明</span><span class="sxs-lookup"><span data-stu-id="1cb81-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb81-106">AzureRmApiManagementOperation Cmdlet 會移除現有 **的** 操作。</span><span class="sxs-lookup"><span data-stu-id="1cb81-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="1cb81-107">示例</span><span class="sxs-lookup"><span data-stu-id="1cb81-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb81-108">範例1：移除現有的 API 操作</span><span class="sxs-lookup"><span data-stu-id="1cb81-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="1cb81-109">這個命令會移除現有的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="1cb81-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="1cb81-110">參數</span><span class="sxs-lookup"><span data-stu-id="1cb81-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb81-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1cb81-111">-ApiId</span></span>
<span data-ttu-id="1cb81-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cb81-112">Specifies the identifier of the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-113">-內容</span><span class="sxs-lookup"><span data-stu-id="1cb81-113">-Context</span></span>
<span data-ttu-id="1cb81-114">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="1cb81-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb81-115">-DefaultProfile</span></span>
<span data-ttu-id="1cb81-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cb81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1cb81-117">-OperationId</span></span>
<span data-ttu-id="1cb81-118">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cb81-118">Specifies the identifier of the API operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cb81-119">-PassThru</span></span>
<span data-ttu-id="1cb81-120">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="1cb81-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1cb81-121">-Confirm</span></span>
<span data-ttu-id="1cb81-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cb81-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb81-123">-WhatIf</span></span>
<span data-ttu-id="1cb81-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cb81-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb81-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cb81-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb81-126">CommonParameters</span></span>
<span data-ttu-id="1cb81-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cb81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb81-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cb81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb81-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1cb81-129">INPUTS</span></span>

### <span data-ttu-id="1cb81-130">所有</span><span class="sxs-lookup"><span data-stu-id="1cb81-130">None</span></span>
<span data-ttu-id="1cb81-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1cb81-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1cb81-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1cb81-132">OUTPUTS</span></span>

### <span data-ttu-id="1cb81-133">bool</span><span class="sxs-lookup"><span data-stu-id="1cb81-133">bool</span></span>

## <span data-ttu-id="1cb81-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1cb81-134">NOTES</span></span>

## <span data-ttu-id="1cb81-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cb81-135">RELATED LINKS</span></span>

[<span data-ttu-id="1cb81-136">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="1cb81-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="1cb81-137">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="1cb81-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="1cb81-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="1cb81-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


