---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287815"
---
# <span data-ttu-id="f0036-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0036-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="f0036-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0036-102">SYNOPSIS</span></span>
<span data-ttu-id="f0036-103">移除 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="f0036-103">Removes an API Management service.</span></span>

## <span data-ttu-id="f0036-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0036-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0036-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0036-105">DESCRIPTION</span></span>
<span data-ttu-id="f0036-106">**AzApiManagement** Cmdlet 會移除 Azure API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="f0036-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="f0036-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0036-107">EXAMPLES</span></span>

### <span data-ttu-id="f0036-108">範例1：移除 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="f0036-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="f0036-109">這個命令會移除名為 ContosoApi 的 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="f0036-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="f0036-110">參數</span><span class="sxs-lookup"><span data-stu-id="f0036-110">PARAMETERS</span></span>

### <span data-ttu-id="f0036-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0036-111">-DefaultProfile</span></span>
<span data-ttu-id="f0036-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0036-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0036-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0036-113">-Name</span></span>
<span data-ttu-id="f0036-114">指定此 Cmdlet 移除之 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0036-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0036-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0036-115">-PassThru</span></span>
<span data-ttu-id="f0036-116">表示此 Cmdlet 會傳回 $True 的值（如果操作成功的話）。</span><span class="sxs-lookup"><span data-stu-id="f0036-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0036-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0036-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0036-118">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0036-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="f0036-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f0036-119">-Confirm</span></span>
<span data-ttu-id="f0036-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0036-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0036-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0036-121">-WhatIf</span></span>
<span data-ttu-id="f0036-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0036-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0036-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0036-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0036-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0036-124">CommonParameters</span></span>
<span data-ttu-id="f0036-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0036-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0036-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0036-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0036-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f0036-127">INPUTS</span></span>

### <span data-ttu-id="f0036-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f0036-128">System.String</span></span>

## <span data-ttu-id="f0036-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f0036-129">OUTPUTS</span></span>

### <span data-ttu-id="f0036-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f0036-130">System.Boolean</span></span>

## <span data-ttu-id="f0036-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f0036-131">NOTES</span></span>

## <span data-ttu-id="f0036-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0036-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0036-133">備份-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0036-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f0036-134">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0036-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="f0036-135">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0036-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f0036-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0036-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


