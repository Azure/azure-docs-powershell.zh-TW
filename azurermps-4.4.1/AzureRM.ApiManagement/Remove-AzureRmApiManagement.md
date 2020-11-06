---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445208"
---
# <span data-ttu-id="54743-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54743-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="54743-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54743-102">SYNOPSIS</span></span>
<span data-ttu-id="54743-103">移除 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="54743-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54743-104">句法</span><span class="sxs-lookup"><span data-stu-id="54743-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54743-105">說明</span><span class="sxs-lookup"><span data-stu-id="54743-105">DESCRIPTION</span></span>
<span data-ttu-id="54743-106">**AzureRmApiManagement** Cmdlet 會移除 Azure API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="54743-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="54743-107">示例</span><span class="sxs-lookup"><span data-stu-id="54743-107">EXAMPLES</span></span>

### <span data-ttu-id="54743-108">範例1：移除 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="54743-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="54743-109">這個命令會移除名為 ContosoApi 的 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="54743-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="54743-110">參數</span><span class="sxs-lookup"><span data-stu-id="54743-110">PARAMETERS</span></span>

### <span data-ttu-id="54743-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="54743-111">-Name</span></span>
<span data-ttu-id="54743-112">指定此 Cmdlet 移除之 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="54743-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="54743-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54743-113">-PassThru</span></span>
<span data-ttu-id="54743-114">表示此 Cmdlet 會傳回 $True 的值（如果操作成功的話）。</span><span class="sxs-lookup"><span data-stu-id="54743-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="54743-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54743-115">-ResourceGroupName</span></span>
<span data-ttu-id="54743-116">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54743-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="54743-117">-確認</span><span class="sxs-lookup"><span data-stu-id="54743-117">-Confirm</span></span>
<span data-ttu-id="54743-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54743-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54743-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54743-119">-WhatIf</span></span>
<span data-ttu-id="54743-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54743-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54743-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54743-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54743-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54743-122">-DefaultProfile</span></span>
<span data-ttu-id="54743-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54743-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54743-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54743-124">CommonParameters</span></span>
<span data-ttu-id="54743-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54743-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54743-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54743-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54743-127">輸入</span><span class="sxs-lookup"><span data-stu-id="54743-127">INPUTS</span></span>

## <span data-ttu-id="54743-128">輸出</span><span class="sxs-lookup"><span data-stu-id="54743-128">OUTPUTS</span></span>

### <span data-ttu-id="54743-129">System.object</span><span class="sxs-lookup"><span data-stu-id="54743-129">System.Boolean</span></span>

## <span data-ttu-id="54743-130">筆記</span><span class="sxs-lookup"><span data-stu-id="54743-130">NOTES</span></span>

## <span data-ttu-id="54743-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="54743-131">RELATED LINKS</span></span>

[<span data-ttu-id="54743-132">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54743-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="54743-133">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54743-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="54743-134">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54743-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="54743-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54743-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


