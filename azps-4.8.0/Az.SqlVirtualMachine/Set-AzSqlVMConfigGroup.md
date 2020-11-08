---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128034"
---
# <span data-ttu-id="9d81c-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="9d81c-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="9d81c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d81c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d81c-103">在 sql 虛擬機器設定中設定相對於 sql 虛擬電腦群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="9d81c-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="9d81c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d81c-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d81c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d81c-105">DESCRIPTION</span></span>
<span data-ttu-id="9d81c-106">Set-AzSqlVMConfigGroup Cmdlet 設定為加入 sql 虛擬機器設定的 sql 虛擬電腦群組所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="9d81c-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="9d81c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d81c-107">EXAMPLES</span></span>

### <span data-ttu-id="9d81c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9d81c-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="9d81c-109">更新 sql 虛擬機器設定的群組擁有情況。</span><span class="sxs-lookup"><span data-stu-id="9d81c-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="9d81c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d81c-110">PARAMETERS</span></span>

### <span data-ttu-id="9d81c-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="9d81c-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="9d81c-112">[群集引導] 帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="9d81c-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d81c-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="9d81c-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="9d81c-114">[群集] 操作員帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="9d81c-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d81c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d81c-115">-DefaultProfile</span></span>
<span data-ttu-id="9d81c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d81c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d81c-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="9d81c-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="9d81c-118">SQL 服務帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="9d81c-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d81c-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="9d81c-119">-SqlVM</span></span>
<span data-ttu-id="9d81c-120">將新增群組成員資格的 SQL 虛擬機器設定</span><span class="sxs-lookup"><span data-stu-id="9d81c-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d81c-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="9d81c-121">-SqlVMGroup</span></span>
<span data-ttu-id="9d81c-122">SQL 虛擬機器所屬的群組</span><span class="sxs-lookup"><span data-stu-id="9d81c-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d81c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d81c-123">CommonParameters</span></span>
<span data-ttu-id="9d81c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d81c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d81c-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d81c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d81c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9d81c-126">INPUTS</span></span>

### <span data-ttu-id="9d81c-127">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="9d81c-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="9d81c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9d81c-128">OUTPUTS</span></span>

### <span data-ttu-id="9d81c-129">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="9d81c-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="9d81c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9d81c-130">NOTES</span></span>

## <span data-ttu-id="9d81c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d81c-131">RELATED LINKS</span></span>
