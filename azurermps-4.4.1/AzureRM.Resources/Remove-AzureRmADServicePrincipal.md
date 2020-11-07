---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625072"
---
# <span data-ttu-id="7d5bc-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d5bc-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="7d5bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5bc-103">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d5bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d5bc-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d5bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="7d5bc-106">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="7d5bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="7d5bc-108">--------------------------刪除 AAD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="7d5bc-109">刪除指定的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="7d5bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d5bc-110">PARAMETERS</span></span>

### <span data-ttu-id="7d5bc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7d5bc-111">-Force</span></span>
<span data-ttu-id="7d5bc-112">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="7d5bc-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="7d5bc-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7d5bc-113">-ObjectId</span></span>
<span data-ttu-id="7d5bc-114">要刪除的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5bc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d5bc-115">-PassThru</span></span>
<span data-ttu-id="7d5bc-116">如果已指定，則傳回已刪除的服務主體。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="7d5bc-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7d5bc-117">-Confirm</span></span>
<span data-ttu-id="7d5bc-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d5bc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d5bc-119">-WhatIf</span></span>
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

### <span data-ttu-id="7d5bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5bc-120">-DefaultProfile</span></span>
<span data-ttu-id="7d5bc-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d5bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5bc-122">CommonParameters</span></span>
<span data-ttu-id="7d5bc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5bc-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d5bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5bc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7d5bc-125">INPUTS</span></span>

## <span data-ttu-id="7d5bc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7d5bc-126">OUTPUTS</span></span>

### <span data-ttu-id="7d5bc-127">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d5bc-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="7d5bc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7d5bc-128">NOTES</span></span>
<span data-ttu-id="7d5bc-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="7d5bc-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7d5bc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d5bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d5bc-131">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d5bc-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="7d5bc-132">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d5bc-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="7d5bc-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d5bc-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="7d5bc-134">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7d5bc-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="7d5bc-135">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7d5bc-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
