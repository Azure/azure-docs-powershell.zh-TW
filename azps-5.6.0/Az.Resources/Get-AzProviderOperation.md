---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917933"
---
# <span data-ttu-id="52d44-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="52d44-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="52d44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52d44-102">SYNOPSIS</span></span>
<span data-ttu-id="52d44-103">取得使用 Azure RBAC 可保護的 Azure 資源提供者的作業。</span><span class="sxs-lookup"><span data-stu-id="52d44-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="52d44-104">語法</span><span class="sxs-lookup"><span data-stu-id="52d44-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52d44-105">描述</span><span class="sxs-lookup"><span data-stu-id="52d44-105">DESCRIPTION</span></span>
<span data-ttu-id="52d44-106">此Get-AzProviderOperation會由 Azure 資源提供者公開作業。</span><span class="sxs-lookup"><span data-stu-id="52d44-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="52d44-107">您可以撰寫作業，以在 Azure RBAC 中建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="52d44-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="52d44-108">該命令會使用可能的萬用字元 (輸入操作搜尋字串 () 字元 (字元) ) 決定要顯示的 *作業詳細資料。使用 Get-AzProviderOperation \* 取得所有 Azure 資源提供者的所有作業。使用 Get-AzProviderOperation Microsoft.Compute/* 取得 Microsoft.Compute 資源提供者的所有作業。</span><span class="sxs-lookup"><span data-stu-id="52d44-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="52d44-109">例子</span><span class="sxs-lookup"><span data-stu-id="52d44-109">EXAMPLES</span></span>

### <span data-ttu-id="52d44-110">範例 1：取得所有提供者的所有動作</span><span class="sxs-lookup"><span data-stu-id="52d44-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="52d44-111">範例 2：取得特定資源提供者的動作</span><span class="sxs-lookup"><span data-stu-id="52d44-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="52d44-112">範例 3：取得可在虛擬機器上執行的所有動作</span><span class="sxs-lookup"><span data-stu-id="52d44-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="52d44-113">參數</span><span class="sxs-lookup"><span data-stu-id="52d44-113">PARAMETERS</span></span>

### <span data-ttu-id="52d44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d44-114">-DefaultProfile</span></span>
<span data-ttu-id="52d44-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="52d44-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52d44-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="52d44-116">-OperationSearchString</span></span>
<span data-ttu-id="52d44-117">操作搜尋字串 (包含可能的萬用字元 (\*) 字元) </span><span class="sxs-lookup"><span data-stu-id="52d44-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d44-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d44-118">CommonParameters</span></span>
<span data-ttu-id="52d44-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52d44-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d44-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52d44-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d44-121">輸入</span><span class="sxs-lookup"><span data-stu-id="52d44-121">INPUTS</span></span>

### <span data-ttu-id="52d44-122">System.String</span><span class="sxs-lookup"><span data-stu-id="52d44-122">System.String</span></span>

## <span data-ttu-id="52d44-123">輸出</span><span class="sxs-lookup"><span data-stu-id="52d44-123">OUTPUTS</span></span>

### <span data-ttu-id="52d44-124">Microsoft.Azure.Commands.Resources.models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="52d44-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="52d44-125">筆記</span><span class="sxs-lookup"><span data-stu-id="52d44-125">NOTES</span></span>
<span data-ttu-id="52d44-126">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="52d44-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="52d44-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="52d44-127">RELATED LINKS</span></span>
