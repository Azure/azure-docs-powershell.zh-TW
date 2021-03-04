---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: f1b5d95397aad24b84462c7e9ceba4a06ba854c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912869"
---
# <span data-ttu-id="09bf9-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="09bf9-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="09bf9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="09bf9-103">在 DevTest 實驗室中，獲得實驗室的允許虛擬機器大小政策。</span><span class="sxs-lookup"><span data-stu-id="09bf9-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="09bf9-104">語法</span><span class="sxs-lookup"><span data-stu-id="09bf9-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09bf9-105">描述</span><span class="sxs-lookup"><span data-stu-id="09bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="09bf9-106">**Get-AzDtlAllowedMSizesPolicy** Cmdlet 會取得允許的虛擬機器大小政策，這可讓您指定實驗室中允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="09bf9-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="09bf9-107">Cmdlet 會返回該策略的啟用或停用狀態，以及您于指定政策中設定的所有允許虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="09bf9-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="09bf9-108">例子</span><span class="sxs-lookup"><span data-stu-id="09bf9-108">EXAMPLES</span></span>

## <span data-ttu-id="09bf9-109">參數</span><span class="sxs-lookup"><span data-stu-id="09bf9-109">PARAMETERS</span></span>

### <span data-ttu-id="09bf9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bf9-110">-DefaultProfile</span></span>
<span data-ttu-id="09bf9-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09bf9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09bf9-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="09bf9-112">-LabName</span></span>
<span data-ttu-id="09bf9-113">指定此 Cmdlet 會獲得虛擬機器大小策略的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="09bf9-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bf9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09bf9-114">-ResourceGroupName</span></span>
<span data-ttu-id="09bf9-115">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09bf9-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bf9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bf9-116">CommonParameters</span></span>
<span data-ttu-id="09bf9-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09bf9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bf9-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09bf9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bf9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="09bf9-119">INPUTS</span></span>

### <span data-ttu-id="09bf9-120">System.String</span><span class="sxs-lookup"><span data-stu-id="09bf9-120">System.String</span></span>

## <span data-ttu-id="09bf9-121">輸出</span><span class="sxs-lookup"><span data-stu-id="09bf9-121">OUTPUTS</span></span>

### <span data-ttu-id="09bf9-122">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="09bf9-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="09bf9-123">筆記</span><span class="sxs-lookup"><span data-stu-id="09bf9-123">NOTES</span></span>

## <span data-ttu-id="09bf9-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="09bf9-124">RELATED LINKS</span></span>

[<span data-ttu-id="09bf9-125">Set-AzDtlAllowedMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="09bf9-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


