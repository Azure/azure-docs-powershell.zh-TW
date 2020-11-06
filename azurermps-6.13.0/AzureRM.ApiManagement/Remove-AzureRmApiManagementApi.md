---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cf27d54e50d320d0ad20a3e847cf2b9dda8ac3c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451952"
---
# <span data-ttu-id="36325-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="36325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36325-102">SYNOPSIS</span></span>
<span data-ttu-id="36325-103">移除 API。</span><span class="sxs-lookup"><span data-stu-id="36325-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36325-104">句法</span><span class="sxs-lookup"><span data-stu-id="36325-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36325-105">說明</span><span class="sxs-lookup"><span data-stu-id="36325-105">DESCRIPTION</span></span>
<span data-ttu-id="36325-106">AzureRmApiManagementApi Cmdlet 會移除現有 **的** API。</span><span class="sxs-lookup"><span data-stu-id="36325-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="36325-107">示例</span><span class="sxs-lookup"><span data-stu-id="36325-107">EXAMPLES</span></span>

### <span data-ttu-id="36325-108">範例1：移除 API</span><span class="sxs-lookup"><span data-stu-id="36325-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="36325-109">這個命令會移除具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="36325-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="36325-110">參數</span><span class="sxs-lookup"><span data-stu-id="36325-110">PARAMETERS</span></span>

### <span data-ttu-id="36325-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="36325-111">-ApiId</span></span>
<span data-ttu-id="36325-112">指定 API 移除的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36325-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="36325-113">-內容</span><span class="sxs-lookup"><span data-stu-id="36325-113">-Context</span></span>
<span data-ttu-id="36325-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="36325-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36325-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36325-115">-DefaultProfile</span></span>
<span data-ttu-id="36325-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36325-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36325-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36325-117">-PassThru</span></span>
<span data-ttu-id="36325-118">passthru</span><span class="sxs-lookup"><span data-stu-id="36325-118">passthru</span></span>

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

### <span data-ttu-id="36325-119">-確認</span><span class="sxs-lookup"><span data-stu-id="36325-119">-Confirm</span></span>
<span data-ttu-id="36325-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36325-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36325-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36325-121">-WhatIf</span></span>
<span data-ttu-id="36325-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36325-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36325-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36325-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36325-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36325-124">CommonParameters</span></span>
<span data-ttu-id="36325-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36325-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36325-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36325-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36325-127">輸入</span><span class="sxs-lookup"><span data-stu-id="36325-127">INPUTS</span></span>

### <span data-ttu-id="36325-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="36325-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36325-129">System.object</span><span class="sxs-lookup"><span data-stu-id="36325-129">System.String</span></span>

### <span data-ttu-id="36325-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="36325-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36325-131">輸出</span><span class="sxs-lookup"><span data-stu-id="36325-131">OUTPUTS</span></span>

### <span data-ttu-id="36325-132">System.object</span><span class="sxs-lookup"><span data-stu-id="36325-132">System.Boolean</span></span>

## <span data-ttu-id="36325-133">筆記</span><span class="sxs-lookup"><span data-stu-id="36325-133">NOTES</span></span>

## <span data-ttu-id="36325-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="36325-134">RELATED LINKS</span></span>

[<span data-ttu-id="36325-135">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-135">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="36325-136">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="36325-137">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-137">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="36325-138">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-138">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="36325-139">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="36325-139">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


