---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911722"
---
# <span data-ttu-id="2ee36-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="2ee36-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="2ee36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ee36-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee36-103">取得 Azure 容器註冊表的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2ee36-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="2ee36-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ee36-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee36-105">描述</span><span class="sxs-lookup"><span data-stu-id="2ee36-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee36-106">取得 Azure 容器註冊表的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2ee36-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="2ee36-107">例子</span><span class="sxs-lookup"><span data-stu-id="2ee36-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee36-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ee36-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="2ee36-109">取得 Azure 容器註冊表的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2ee36-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="2ee36-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ee36-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee36-111">-DefaultProfile</span></span>
<span data-ttu-id="2ee36-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ee36-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee36-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ee36-113">-Name</span></span>
<span data-ttu-id="2ee36-114">目標注冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee36-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee36-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee36-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ee36-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2ee36-116">Resource group name.</span></span>

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

### <span data-ttu-id="2ee36-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee36-117">CommonParameters</span></span>
<span data-ttu-id="2ee36-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ee36-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee36-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee36-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee36-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2ee36-120">INPUTS</span></span>

### <span data-ttu-id="2ee36-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2ee36-121">System.String</span></span>

## <span data-ttu-id="2ee36-122">輸出</span><span class="sxs-lookup"><span data-stu-id="2ee36-122">OUTPUTS</span></span>

### <span data-ttu-id="2ee36-123">Microsoft.Azure.Commands.ContainerRegistry.models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="2ee36-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="2ee36-124">筆記</span><span class="sxs-lookup"><span data-stu-id="2ee36-124">NOTES</span></span>

## <span data-ttu-id="2ee36-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ee36-125">RELATED LINKS</span></span>
