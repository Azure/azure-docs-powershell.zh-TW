---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624668"
---
# <span data-ttu-id="a7b45-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7b45-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="a7b45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7b45-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b45-103">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="a7b45-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7b45-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7b45-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b45-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7b45-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b45-106">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="a7b45-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="a7b45-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7b45-107">EXAMPLES</span></span>

### <span data-ttu-id="a7b45-108">刪除 AAD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="a7b45-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="a7b45-109">刪除指定的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="a7b45-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="a7b45-110">參數</span><span class="sxs-lookup"><span data-stu-id="a7b45-110">PARAMETERS</span></span>

### <span data-ttu-id="a7b45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b45-111">-DefaultProfile</span></span>
<span data-ttu-id="a7b45-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a7b45-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7b45-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a7b45-113">-Force</span></span>
<span data-ttu-id="a7b45-114">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="a7b45-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="a7b45-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a7b45-115">-ObjectId</span></span>
<span data-ttu-id="a7b45-116">要刪除的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7b45-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b45-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7b45-117">-PassThru</span></span>
<span data-ttu-id="a7b45-118">如果已指定，則傳回已刪除的服務主體。</span><span class="sxs-lookup"><span data-stu-id="a7b45-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="a7b45-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a7b45-119">-Confirm</span></span>
<span data-ttu-id="a7b45-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7b45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b45-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b45-121">-WhatIf</span></span>
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

### <span data-ttu-id="a7b45-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b45-122">CommonParameters</span></span>
<span data-ttu-id="a7b45-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7b45-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b45-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7b45-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b45-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a7b45-125">INPUTS</span></span>

### <span data-ttu-id="a7b45-126">所有</span><span class="sxs-lookup"><span data-stu-id="a7b45-126">None</span></span>
<span data-ttu-id="a7b45-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a7b45-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7b45-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a7b45-128">OUTPUTS</span></span>

### <span data-ttu-id="a7b45-129">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7b45-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a7b45-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a7b45-130">NOTES</span></span>
<span data-ttu-id="a7b45-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="a7b45-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a7b45-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7b45-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7b45-133">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7b45-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a7b45-134">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7b45-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a7b45-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7b45-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a7b45-136">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a7b45-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="a7b45-137">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a7b45-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
