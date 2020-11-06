---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445191"
---
# <span data-ttu-id="ad2ab-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ad2ab-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="ad2ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2ab-103">移除 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad2ab-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad2ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2ab-106">**AzureRmApiManagementProperty** Cmdlet 會移除 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="ad2ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad2ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2ab-108">範例1：移除屬性</span><span class="sxs-lookup"><span data-stu-id="ad2ab-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="ad2ab-109">這個命令會移除 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="ad2ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad2ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ad2ab-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ad2ab-111">-Context</span></span>
<span data-ttu-id="ad2ab-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ad2ab-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad2ab-113">-PassThru</span></span>
<span data-ttu-id="ad2ab-114">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="ad2ab-115">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ad2ab-115">-PropertyId</span></span>
<span data-ttu-id="ad2ab-116">指定此 Cmdlet 移除之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad2ab-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ad2ab-117">-Confirm</span></span>
<span data-ttu-id="ad2ab-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2ab-119">-WhatIf</span></span>
<span data-ttu-id="ad2ab-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2ab-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2ab-122">-DefaultProfile</span></span>
<span data-ttu-id="ad2ab-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2ab-124">CommonParameters</span></span>
<span data-ttu-id="ad2ab-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2ab-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad2ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ad2ab-127">INPUTS</span></span>

## <span data-ttu-id="ad2ab-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ad2ab-128">OUTPUTS</span></span>

### <span data-ttu-id="ad2ab-129">bool</span><span class="sxs-lookup"><span data-stu-id="ad2ab-129">bool</span></span>

## <span data-ttu-id="ad2ab-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ad2ab-130">NOTES</span></span>

## <span data-ttu-id="ad2ab-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad2ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad2ab-132">新-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ad2ab-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="ad2ab-133">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ad2ab-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


