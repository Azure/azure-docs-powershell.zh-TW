---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452371"
---
# <span data-ttu-id="5eea9-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5eea9-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="5eea9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5eea9-102">SYNOPSIS</span></span>
<span data-ttu-id="5eea9-103">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5eea9-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eea9-104">句法</span><span class="sxs-lookup"><span data-stu-id="5eea9-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eea9-105">說明</span><span class="sxs-lookup"><span data-stu-id="5eea9-105">DESCRIPTION</span></span>
<span data-ttu-id="5eea9-106">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5eea9-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5eea9-107">示例</span><span class="sxs-lookup"><span data-stu-id="5eea9-107">EXAMPLES</span></span>

### <span data-ttu-id="5eea9-108">--------------------------[刪除 AAD 應用程式]。</span><span class="sxs-lookup"><span data-stu-id="5eea9-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="5eea9-109">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5eea9-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5eea9-110">參數</span><span class="sxs-lookup"><span data-stu-id="5eea9-110">PARAMETERS</span></span>

### <span data-ttu-id="5eea9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5eea9-111">-Force</span></span>
<span data-ttu-id="5eea9-112">切換以刪除應用程式而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="5eea9-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="5eea9-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5eea9-113">-ObjectId</span></span>
<span data-ttu-id="5eea9-114">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5eea9-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eea9-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5eea9-115">-Confirm</span></span>
<span data-ttu-id="5eea9-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5eea9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eea9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eea9-117">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eea9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eea9-118">-DefaultProfile</span></span>
<span data-ttu-id="5eea9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eea9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eea9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eea9-120">CommonParameters</span></span>
<span data-ttu-id="5eea9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5eea9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eea9-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5eea9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eea9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5eea9-123">INPUTS</span></span>

## <span data-ttu-id="5eea9-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5eea9-124">OUTPUTS</span></span>

## <span data-ttu-id="5eea9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5eea9-125">NOTES</span></span>
<span data-ttu-id="5eea9-126">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="5eea9-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5eea9-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eea9-127">RELATED LINKS</span></span>

[<span data-ttu-id="5eea9-128">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5eea9-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="5eea9-129">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5eea9-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="5eea9-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5eea9-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="5eea9-131">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5eea9-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

