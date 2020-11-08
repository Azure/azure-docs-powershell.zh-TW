---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971006"
---
# <span data-ttu-id="81148-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81148-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="81148-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81148-102">SYNOPSIS</span></span>
<span data-ttu-id="81148-103">取得 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="81148-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="81148-104">句法</span><span class="sxs-lookup"><span data-stu-id="81148-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81148-105">說明</span><span class="sxs-lookup"><span data-stu-id="81148-105">DESCRIPTION</span></span>
<span data-ttu-id="81148-106">取得 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="81148-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="81148-107">示例</span><span class="sxs-lookup"><span data-stu-id="81148-107">EXAMPLES</span></span>

### <span data-ttu-id="81148-108">範例1</span><span class="sxs-lookup"><span data-stu-id="81148-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="81148-109">取得目前的管理合作夥伴識別碼</span><span class="sxs-lookup"><span data-stu-id="81148-109">Get the current management partner id</span></span>

### <span data-ttu-id="81148-110">範例2</span><span class="sxs-lookup"><span data-stu-id="81148-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="81148-111">使用合作夥伴識別碼取得目前的管理合作夥伴識別碼（如果不相符），則會失敗</span><span class="sxs-lookup"><span data-stu-id="81148-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="81148-112">參數</span><span class="sxs-lookup"><span data-stu-id="81148-112">PARAMETERS</span></span>

### <span data-ttu-id="81148-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81148-113">-DefaultProfile</span></span>
<span data-ttu-id="81148-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81148-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81148-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="81148-115">-PartnerId</span></span>
<span data-ttu-id="81148-116">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="81148-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81148-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81148-117">CommonParameters</span></span>
<span data-ttu-id="81148-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81148-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81148-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81148-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81148-120">輸入</span><span class="sxs-lookup"><span data-stu-id="81148-120">INPUTS</span></span>

### <span data-ttu-id="81148-121">所有</span><span class="sxs-lookup"><span data-stu-id="81148-121">None</span></span>

## <span data-ttu-id="81148-122">輸出</span><span class="sxs-lookup"><span data-stu-id="81148-122">OUTPUTS</span></span>

### <span data-ttu-id="81148-123">PSManagementPartner 中的 ManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81148-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="81148-124">筆記</span><span class="sxs-lookup"><span data-stu-id="81148-124">NOTES</span></span>

## <span data-ttu-id="81148-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="81148-125">RELATED LINKS</span></span>

[<span data-ttu-id="81148-126">移除-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81148-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="81148-127">新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81148-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="81148-128">更新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81148-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)