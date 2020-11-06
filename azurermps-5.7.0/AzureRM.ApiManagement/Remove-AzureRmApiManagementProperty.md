---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444812"
---
# <span data-ttu-id="9b94a-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9b94a-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="9b94a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b94a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b94a-103">移除 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="9b94a-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b94a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b94a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b94a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b94a-105">DESCRIPTION</span></span>
<span data-ttu-id="9b94a-106">**AzureRmApiManagementProperty** Cmdlet 會移除 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="9b94a-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="9b94a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b94a-107">EXAMPLES</span></span>

### <span data-ttu-id="9b94a-108">範例1：移除屬性</span><span class="sxs-lookup"><span data-stu-id="9b94a-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="9b94a-109">這個命令會移除 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b94a-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="9b94a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b94a-110">PARAMETERS</span></span>

### <span data-ttu-id="9b94a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="9b94a-111">-Context</span></span>
<span data-ttu-id="9b94a-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b94a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b94a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b94a-113">-DefaultProfile</span></span>
<span data-ttu-id="9b94a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b94a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9b94a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b94a-115">-PassThru</span></span>
<span data-ttu-id="9b94a-116">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="9b94a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="9b94a-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="9b94a-117">-PropertyId</span></span>
<span data-ttu-id="9b94a-118">指定此 Cmdlet 移除之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b94a-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9b94a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9b94a-119">-Confirm</span></span>
<span data-ttu-id="9b94a-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b94a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b94a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b94a-121">-WhatIf</span></span>
<span data-ttu-id="9b94a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b94a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b94a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b94a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b94a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b94a-124">CommonParameters</span></span>
<span data-ttu-id="9b94a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b94a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b94a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b94a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b94a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b94a-127">INPUTS</span></span>

### <span data-ttu-id="9b94a-128">所有</span><span class="sxs-lookup"><span data-stu-id="9b94a-128">None</span></span>
<span data-ttu-id="9b94a-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9b94a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b94a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9b94a-130">OUTPUTS</span></span>

### <span data-ttu-id="9b94a-131">bool</span><span class="sxs-lookup"><span data-stu-id="9b94a-131">bool</span></span>

## <span data-ttu-id="9b94a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9b94a-132">NOTES</span></span>

## <span data-ttu-id="9b94a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b94a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9b94a-134">新-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9b94a-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="9b94a-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9b94a-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


