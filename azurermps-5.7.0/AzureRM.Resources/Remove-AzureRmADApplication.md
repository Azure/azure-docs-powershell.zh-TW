---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624671"
---
# <span data-ttu-id="de3b4-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="de3b4-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="de3b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="de3b4-103">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="de3b4-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="de3b4-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="de3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="de3b4-106">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="de3b4-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="de3b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="de3b4-107">EXAMPLES</span></span>

### <span data-ttu-id="de3b4-108">刪除 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="de3b4-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="de3b4-109">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="de3b4-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="de3b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="de3b4-110">PARAMETERS</span></span>

### <span data-ttu-id="de3b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3b4-111">-DefaultProfile</span></span>
<span data-ttu-id="de3b4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="de3b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de3b4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de3b4-113">-Force</span></span>
<span data-ttu-id="de3b4-114">切換以刪除應用程式而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="de3b4-114">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3b4-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="de3b4-115">-ObjectId</span></span>
<span data-ttu-id="de3b4-116">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="de3b4-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b4-117">-確認</span><span class="sxs-lookup"><span data-stu-id="de3b4-117">-Confirm</span></span>
<span data-ttu-id="de3b4-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de3b4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3b4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3b4-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3b4-120">CommonParameters</span></span>
<span data-ttu-id="de3b4-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de3b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3b4-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de3b4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3b4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="de3b4-123">INPUTS</span></span>

### <span data-ttu-id="de3b4-124">所有</span><span class="sxs-lookup"><span data-stu-id="de3b4-124">None</span></span>
<span data-ttu-id="de3b4-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="de3b4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de3b4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="de3b4-126">OUTPUTS</span></span>

## <span data-ttu-id="de3b4-127">筆記</span><span class="sxs-lookup"><span data-stu-id="de3b4-127">NOTES</span></span>
<span data-ttu-id="de3b4-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="de3b4-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="de3b4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="de3b4-129">RELATED LINKS</span></span>

[<span data-ttu-id="de3b4-130">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="de3b4-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="de3b4-131">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="de3b4-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="de3b4-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="de3b4-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="de3b4-133">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="de3b4-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

