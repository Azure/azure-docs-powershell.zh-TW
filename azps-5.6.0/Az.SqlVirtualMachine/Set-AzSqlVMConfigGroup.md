---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: 4dd2042ae3c7e84b9a7a82dde19fb5848229f51c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905738"
---
# <span data-ttu-id="a9203-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="a9203-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="a9203-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9203-102">SYNOPSIS</span></span>
<span data-ttu-id="a9203-103">在 sql 虛擬機器設定中設定與 sql 虛擬機器群組相對的資訊。</span><span class="sxs-lookup"><span data-stu-id="a9203-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a9203-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9203-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9203-105">描述</span><span class="sxs-lookup"><span data-stu-id="a9203-105">DESCRIPTION</span></span>
<span data-ttu-id="a9203-106">Cmdlet Set-AzSqlVMConfigGroup設定加入 sql 虛擬機器群組以設定 sql 虛擬機器所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="a9203-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a9203-107">例子</span><span class="sxs-lookup"><span data-stu-id="a9203-107">EXAMPLES</span></span>

### <span data-ttu-id="a9203-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9203-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="a9203-109">更新 sql 虛擬機器配置的群組資訊。</span><span class="sxs-lookup"><span data-stu-id="a9203-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="a9203-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9203-110">PARAMETERS</span></span>

### <span data-ttu-id="a9203-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a9203-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="a9203-112">組群開機帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="a9203-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="a9203-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a9203-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="a9203-114">組組運算子帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="a9203-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="a9203-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9203-115">-DefaultProfile</span></span>
<span data-ttu-id="a9203-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9203-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9203-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a9203-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="a9203-118">SQL 服務帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="a9203-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="a9203-119">-SqlQL</span><span class="sxs-lookup"><span data-stu-id="a9203-119">-SqlVM</span></span>
<span data-ttu-id="a9203-120">要新增群組成員資格的 SQL 虛擬機器組組</span><span class="sxs-lookup"><span data-stu-id="a9203-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="a9203-121">-SqlQLGROUP</span><span class="sxs-lookup"><span data-stu-id="a9203-121">-SqlVMGroup</span></span>
<span data-ttu-id="a9203-122">SQL 虛擬機器的群組將屬於</span><span class="sxs-lookup"><span data-stu-id="a9203-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="a9203-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9203-123">CommonParameters</span></span>
<span data-ttu-id="a9203-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9203-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9203-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9203-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9203-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a9203-126">INPUTS</span></span>

### <span data-ttu-id="a9203-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="a9203-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a9203-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a9203-128">OUTPUTS</span></span>

### <span data-ttu-id="a9203-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="a9203-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a9203-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a9203-130">NOTES</span></span>

## <span data-ttu-id="a9203-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9203-131">RELATED LINKS</span></span>
